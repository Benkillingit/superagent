# Superagent 👻 — Free AI Clone

A public, static clone of a personal AI agent (originally built on Base44 Superagent). It runs **entirely in your browser** — no server, no accounts, no tracking, zero setup.

## ⚠ Everything here is public by design

- Your messages are sent to a third-party AI provider (Pollinations by default, or Google/xAI/OpenRouter if you bring your own key).
- With GitHub sync on, the whole conversation is saved to a **public GitHub repo** (a `conversations/` folder), visible to anyone.
- Don't type anything private into this chat.

## How to use

1. Open the site. Type. That's it — zero-setup mode uses a free keyless AI API.
2. (Optional, better brains) Settings → paste a free Gemini key from [aistudio.google.com](https://aistudio.google.com/apikey), or an xAI / OpenRouter key.
3. (Optional, public memory) Settings → GitHub Memory → paste a fine-grained GitHub PAT with **Contents: read & write** on the repo. Turn on auto-save and every reply is committed to the public `conversations/` folder — your chat history lives on GitHub and follows you across devices. Load any past session back with "Load a conversation".

## Privacy & security

- API keys and GitHub tokens are stored **only in your browser's localStorage** and sent only to the services you explicitly picked.
- No key or token is embedded in this repo. No analytics, no backend, no server-side logging.
- The AI provider sees your messages; GitHub sees your synced conversations; that's the whole notice.

## Features

- Zero setup, keyless chat out of the box
- 🌐 Web access toggle: the clone can search the internet (Gemini + Google Search grounding)
- Multi-provider: Pollinations (free, no key) / Google Gemini / xAI Grok / OpenRouter free models
- Gemini safety settings set to the loosest the API allows
- Editable system prompt (the personality is yours to rewrite)
- Public GitHub memory sync: auto-save, manual save, session list, restore
- Dark ghost theme, mobile-friendly, markdown-lite, typing indicator
- Quick links to [Benkillingit](https://github.com/Benkillingit) and [APAX 3.0](https://github.com/Benkillingit/apax3)

## Run it yourself

Single `index.html` — download it and open it in any browser, or host anywhere static:

```bash
git clone https://github.com/Benkillingit/superagent.git
cd superagent
# open index.html
```

## Credits

Personality and design cloned from a Base44 Superagent with its owner's blessing. MIT licensed.
