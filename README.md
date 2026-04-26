# Knox — Remember Everything

Knox is a session memory and credential vault for people who use AI assistants regularly. It solves one problem: AI has no memory between conversations, so you end up re-explaining your projects, conventions, and decisions every single session.

Knox keeps one structured record of everything your AI needs to know, and generates a ready-to-paste briefing at the start of each session.

**Works with Claude, ChatGPT, Gemini, Copilot, or any AI assistant.**

🌐 **Live:** https://knox-public.onrender.com

---

## How it works

1. **Set up once** — tell Knox your projects, rules, and any services you use
2. **Generate a briefing** — one click, Knox produces a structured session prompt
3. **Paste and go** — paste into any AI conversation, pick up where you left off

---

## Features

- Session briefing generator — plain text, works with any AI
- Project tracker with decision log and open tasks
- Session rules — tell AI how to behave, auto-included in every briefing
- Credential vault — API keys, service URLs, expiry warnings, environment tags
- Team and family support — share vault via export/import
- PIN protection with email reset
- No account, no server, no subscription

---

## Getting started

**Option 1 — Try it live**
Visit https://knox-public.onrender.com and use it immediately in your browser.

**Option 2 — Download**
Download `app.html` and open it locally. Everything runs in your browser — no server needed.

**Option 3 — Self-host**
Fork this repo and deploy to Render, Netlify, Vercel, or any static host. No build step required — point the service at the repo root and set `index.html` as the entry point.

---

## Privacy & Security

Knox stores all data in your browser's **localStorage**. Nothing is sent to any server. Nothing leaves your device unless you explicitly export it.

The exported backup file is plain JSON. Treat it like a password file — share only via trusted channels (Signal, WhatsApp, encrypted email).

**Knox is not a substitute for a dedicated secrets manager in production environments.** It is designed for personal and small-team use on trusted devices. Always keep backup exports. The authors accept no liability for credential loss or exposure.

---

## PIN reset via email

Knox can send PIN reset codes via [EmailJS](https://emailjs.com) (free tier available). To enable:

1. Create a free EmailJS account
2. Add an email service and create a template with `{{code}}` and `{{to_email}}` variables — set the To Email field to `{{to_email}}`
3. Add your Service ID, Template ID, and Public Key in Knox → Settings

Without EmailJS, forgotten PINs require clearing Knox and re-importing from a backup.

---

## Self-hosting on Render

1. Fork this repo
2. Create a new **Static Site** on [Render](https://render.com)
3. Connect your fork (or deploy as a public repository)
4. Set **Publish directory** to `./`
5. Leave **Build command** blank
6. Deploy

---

## Open source

Knox is licensed under **Creative Commons CC BY-NC 4.0**. Free to use, modify, and share for personal and team use. Commercial use requires permission.

- ✓ Use it for your own work and projects
- ✓ Modify and adapt it
- ✓ Share it with others
- ✗ Sell it or incorporate into a commercial product without permission

For commercial licensing: lance505504@gmail.com

See [LICENSE](./LICENSE) for the full licence text.

---

## Disclaimer

Knox is provided as-is, without warranty of any kind. The authors are not responsible for data loss, credential exposure, or any other damages arising from use of this software. Always maintain backup exports of your vault. Do not use Knox as your sole store of critical credentials.

---

*Built to solve a real problem in real AI-assisted work. Intentionally simple — one file, no dependencies, no backend.*
