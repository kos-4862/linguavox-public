<p align="center">
  <a href="README.md">English</a> · <a href="README.uk.md">Українська</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh-CN.md">中文</a> · <a href="README.es.md">Español</a> · <a href="README.de.md">Deutsch</a> · <a href="README.ja.md">日本語</a>
</p>

<p align="center">
  <img src="https://linguavox-landing.pages.dev/store-screenshots/marquee-1400x560.png" width="800" alt="LinguaVox — AI Voice Dictation Chrome Extension" />
</p>

<h3 align="center">LinguaVox — AI Voice Dictation Chrome Extension</h3>

<p align="center">
  Hold a hotkey · speak · release · text appears in any web field within 3 seconds<br>
  OpenAI Whisper · 21+ languages · No API key required · Slack, Gmail, Notion, Jira
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License" /></a>
  <a href="https://linguavox-landing.pages.dev"><img src="https://img.shields.io/badge/website-linguavox-brightgreen" alt="Website" /></a>
  <a href="https://chromewebstore.google.com/detail/linguavox/TODO"><img src="https://img.shields.io/badge/Chrome%20Web%20Store-Install%20Free-blue?logo=googlechrome" alt="Chrome Web Store" /></a>
  <a href="https://linguavox-landing.pages.dev/dashboard/"><img src="https://img.shields.io/badge/dashboard-open-orange" alt="Dashboard" /></a>
  <a href="https://linguavox-landing.pages.dev/llms.txt"><img src="https://img.shields.io/badge/llms.txt-AI%20docs-purple" alt="llms.txt" /></a>
  <img src="https://img.shields.io/badge/version-2.9-green" alt="Version" />
</p>

---

## What is LinguaVox?

LinguaVox is a Chrome browser extension for AI-powered voice transcription and translation. Users hold a keyboard shortcut (Ctrl+Space), speak, release — and the transcribed text appears instantly in any active text field: chat boxes, email editors, search fields, CRM forms, and code editors. The extension uses OpenAI Whisper for 95%+ accuracy transcription and GPT-4o-mini for optional AI enhancement (grammar correction, style rewriting, translation). Unlike most voice dictation tools that require users to provide their own OpenAI API key, LinguaVox includes a shared key pool — free users get 100 requests per day with zero setup. Power users and teams can bring their own key for unlimited usage.

## How It Works

**Before LinguaVox:** open a separate app → record → copy → switch to browser → paste  
**After LinguaVox:**

```
1. Click any web field (Slack, Gmail, Notion, Jira…)
2. Hold  Ctrl+Space  →  speak
3. Release  →  text appears within ~3 seconds  ✓
```

No copy-paste. No switching apps. Works on any website.

## Where It Works

| Platform | Status | Notes |
|----------|--------|-------|
| Slack (browser) | ✅ | Browser-level hotkey bypass for Slack's key capture |
| Gmail | ✅ | Compose and reply fields |
| Notion | ✅ | All `contenteditable` blocks |
| Jira | ✅ | Issue fields, comments, descriptions |
| Asana | ✅ | Task and comment fields |
| Salesforce | ✅ | CRM input fields |
| Any `<input>` / `<textarea>` | ✅ | Universal — any website |
| Any `contenteditable` | ✅ | React, Draft.js, Quill compatible |
| Google Docs | ⚠️ | Limited — custom canvas editor |

## Architecture

```
 Chrome Extension (MV3)
 ┌──────────────────────────────┐
 │ content.js  — keyboard + UI  │
 │ background.js — orchestration│
 │ popup.js    — settings/auth  │
 └──────────┬───────────────────┘
            │ HTTPS + JWT Bearer
            ▼
 Cloudflare Worker (global edge)
 ┌──────────────────────────────┐
 │ /api/transcribe → Whisper    │
 │ /api/enhance   → GPT-4o-mini │
 │ /api/translate → GPT-4o-mini │
 │ /api/auth      → Google OAuth│
 └──────────┬───────────────────┘
            │
            ▼
 Cloudflare KV
 └─ users · usage counters · orgs
```

All OpenAI API calls go through the Worker. API keys never leave the server.

## Key Features

- **No API key required** — 100 req/day free via shared pool, zero setup
- **Bring Your Own Key** — unlimited usage at OpenAI cost (~$0.50/month typical)
- **Organization accounts** — shared key pool, member management, usage analytics
- **21+ languages** — transcription + translation in one step
- **6 AI enhancement modes** — grammar fix, business style, academic, casual, creative, smart polish
- **Privacy-first** — audio never stored, processed in real-time and discarded
- **Under 3 seconds** — end-to-end from speech to inserted text
- **95%+ accuracy** — OpenAI Whisper large-v2 equivalent

## AI Enhancement Modes

| Mode | What It Does |
|------|-------------|
| Smart Polish | Fix grammar, improve clarity, keep meaning |
| Business Style | Professional communication tone |
| Grammar Fix | Correct grammar and spelling only |
| Creative Style | Vivid, engaging writing |
| Casual Style | Friendly conversational tone |
| Academic Style | Formal academic language |

## Pricing

| Plan | Requests | Setup |
|------|----------|-------|
| Free | 100/day | Google sign-in only |
| Bring Your Own Key | Unlimited | Your OpenAI API key |
| Organization | Unlimited | Shared team key + analytics |

## FAQ

### Does LinguaVox work on Slack?
Yes. Slack intercepts keyboard events at the page level. LinguaVox registers the hotkey at the browser level via `chrome.commands.onCommand`, bypassing Slack's capture. Works in all Slack message fields.

### Do I need an OpenAI API key?
No. Free users get 100 requests/day from the shared pool. Add your own key in the dashboard for unlimited usage.

### Is my voice recorded or stored?
No. Audio is processed in real-time by Whisper and discarded immediately. Zero voice data retained anywhere.

### What languages are supported?
21+ languages: English, Ukrainian, Russian, Spanish, French, German, Japanese, Korean, Chinese, Arabic, Portuguese, Italian, Polish, Dutch, Turkish, Swedish, Romanian, Greek, Tagalog, Urdu, Punjabi, and more.

### How is LinguaVox different from Voice In, Voicy, or BlabbyAI?
LinguaVox is the only extension combining: (1) free tier with no API key, (2) Bring Your Own Key, (3) 6 AI enhancement modes, (4) translation across 21+ languages, and (5) team/org accounts. See [full comparison →](docs/vs-alternatives.md)

## Documentation

| Resource | Description |
|----------|-------------|
| [Use Cases](docs/use-cases.md) | Customer support, devs, non-native speakers, RSI |
| [Integrations](docs/integrations.md) | Platform-specific notes for Slack, Notion, Jira, etc. |
| [vs Alternatives](docs/vs-alternatives.md) | Comparison: Voice In, Voicy, BlabbyAI, Wispr Flow |
| [FAQ](docs/faq.md) | 20+ answers |
| [Changelog](docs/changelog.md) | v1.0 → v2.9 |

## Installation

1. [Chrome Web Store →](https://chromewebstore.google.com/detail/linguavox/TODO) — click "Add to Chrome"
2. Click the LinguaVox icon → "Sign in with Google"
3. Press Ctrl+Space anywhere and start speaking

**For Bring Your Own Key:** [Dashboard → API Key](https://linguavox-landing.pages.dev/dashboard/apikey)

## Links

| | |
|--|--|
| 🌐 Website | https://linguavox-landing.pages.dev |
| 📊 Dashboard | https://linguavox-landing.pages.dev/dashboard/ |
| 🔒 Privacy Policy | https://linguavox-landing.pages.dev/privacy/ |
| 🤖 AI docs (llms.txt) | https://linguavox-landing.pages.dev/llms.txt |
| 💬 Support | https://linguavox-landing.pages.dev/support/ |

## License

MIT — see [LICENSE](LICENSE)