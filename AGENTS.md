# Working in this repo

## What this is

`index.html` is the entire application: one self-contained static page (inline
CSS + inline JS, no bundled assets, no service worker, no external scripts).
There is no `package.json`, no build step, no backend, and no server-side
environment variables.

## Running it (Base44 sandbox)

```bash
docker compose -f docker-compose.base44.yml up -d   # http://localhost:3000
docker compose -f docker-compose.base44.yml logs -f web
docker compose -f docker-compose.base44.yml down
```

`nginx` serves the repo root directly off a bind mount using
`.base44/nginx.conf` (which also denies `/.` paths so `.git` isn't exposed) and
sends `Cache-Control: no-store`.

## Things worth knowing

- **No live-reload dev server exists.** Static files only, so after editing
  `index.html` the browser needs a refresh to show the change.
- **No credentials are needed to run or boot.** The app talks to third-party AI
  APIs directly from the user's browser. The default provider (Pollinations) is
  keyless; Gemini / xAI / OpenRouter keys and the GitHub PAT are optional and
  are typed by the user into the in-page Settings dialog, then kept in
  `localStorage`. They are never read from the environment, so they must not be
  added to the compose file or to `.env` files.
- **Verifying it works:** the page should render the header with a green status
  dot, an empty chat area, a composer at the bottom, and a working Settings
  dialog (provider/model/key fields). The browser console should be free of
  errors; the outbound calls to a provider only happen when a message is sent.
- **The default provider is currently flaky.** Sending a message in zero-setup
  mode calls Pollinations directly from the browser and can come back with a
  server-side `500 ... ENOSPC` from Pollinations itself (their legacy text API is
  also marked deprecated). That is an upstream problem, not a setup failure — the
  app is working when the error bubble renders. Pasting a Gemini / xAI /
  OpenRouter key in Settings is the way to get a real reply.
- **Public by design:** anything typed into the chat (and any repo the user
  points GitHub Memory at) is public. Don't put private data in it while testing.
