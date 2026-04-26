# Knox — Remember Everything

Knox is a session memory and credential vault for people who use AI assistants regularly. It solves one problem: AI has no memory between conversations, so you end up re-explaining your projects, conventions, and decisions every single session.

Knox keeps one structured record of everything your AI needs to know, and generates a ready-to-paste briefing at the start of each session.

**Works with Claude, ChatGPT, Gemini, Copilot, or any AI assistant.**

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
- Credential vault — API keys, service URLs, expiry warnings, env tags
- Team/family support — share vault via encrypted export
- PIN protection with email reset
- No account, no server, no subscription

---

## Getting started

**Option 1 — Try it live**
Visit the hosted version and use it immediately in your browser.

**Option 2 — Download**
Download `app.html` and open it locally. Everything runs in your browser — no server needed. Your data is stored in your browser's localStorage and never leaves your device.

**Option 3 — Self-host**
Fork this repo and deploy to Render, Netlify, Vercel, or any static hosting. Point the service at this repo root and set `index.html` as the entry point.

---

## Privacy

Knox stores all data in your browser's **localStorage**. Nothing is sent to any server. The exported backup file is plain JSON — treat it like a password file and share only via trusted channels.

---

## Setup for PIN reset emails

Knox can send PIN reset codes via [EmailJS](https://emailjs.com) (free tier, 200 emails/month). To enable:

1. Create a free EmailJS account
2. Add an email service and create a template with `{{code}}` and `{{to_email}}` variables
3. Add your Service ID, Template ID, and Public Key in Knox Settings

Without EmailJS configured, forgotten PINs require clearing Knox and re-importing from a backup.

---

## Self-hosting on Render

1. Fork this repo
2. Create a new **Static Site** on [Render](https://render.com)
3. Connect your fork
4. Set **Publish directory** to `/` (root)
5. No build command needed
6. Deploy — done

---

## Licence

MIT. Free to use, modify, and distribute. If you build something useful with it, share it back.

---

*Knox was built to solve a real problem in real AI-assisted development work. It is intentionally simple — one file, no dependencies, no backend.*
