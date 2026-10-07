# Superagent 👻 — Free AI Clone

A public, static clone of a personal AI agent (originally built on Base44 Superagent). It runs **entirely in your browser** — no server, no accounts, no tracking, and it costs nothing to run.

## How to use

1. Get a **free** Google Gemini API key at [aistudio.google.com](https://aistudio.google.com/apikey) (free tier, no card needed). An xAI (Grok) key also works.
2. Open the site, click **Settings**, paste your key.
3. Chat. That's it.

## Privacy & security

- Your API key is stored **only in your browser's localStorage** and sent only to the AI provider you picked (Google or xAI) when you send a message.
- No key is embedded in this repo. No analytics, no backend, no server-side logging.
- Conversation history lives in your browser tab and resets when you clear it.

## Features

- Dark ghost theme, mobile-friendly
- Chat with a personality: warm, low-key, a little gremlin, allergic to filler words
- Provider + model picker (Gemini / Grok), editable system prompt
- Markdown-lite rendering, typing indicator, conversation reset
- Quick links to [Benkillingit](https://github.com/Benkillingit) and [APAX 3.0](https://github.com/Benkillingit/apax3)

## Run it yourself

It's a single `index.html` — download it and open it in any browser. Or clone and host anywhere static (GitHub Pages included):

```bash
git clone https://github.com/Benkillingit/superagent.git
cd superagent
# just open index.html
```

## Credits

Personality and design cloned from a Base44 Superagent with its owner's blessing. MIT licensed — do whatever.
