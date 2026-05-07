<p align="center">
  <a href="README.md">English</a> · <a href="README.uk.md">Українська</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh-CN.md">中文</a> · <a href="README.es.md">Español</a> · <a href="README.de.md">Deutsch</a> · <a href="README.ja.md">日本語</a>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/kos-4862/linguavox-public/main/images/banner.png" width="800" alt="LinguaVox — AI Voice Dictation Chrome Extension" />
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
  <a href="https://linguavox-landing.pages.dev/login"><img src="https://img.shields.io/badge/dashboard-open-orange" alt="Dashboard" /></a>
  <a href="https://linguavox-landing.pages.dev/llms.txt"><img src="https://img.shields.io/badge/llms.txt-AI%20docs-purple" alt="llms.txt" /></a>
  <img src="https://img.shields.io/badge/version-2.8-green" alt="Version" />
</p>

---

## What is LinguaVox?

LinguaVox is a Chrome browser extension for AI-powered voice transcription and translation. Users hold a keyboard shortcut (Ctrl+Space), speak, release — and the transcribed text appears instantly in any active text field: chat boxes, email editors, search fields, CRM forms, and code editors. The extension uses OpenAI Whisper for 95%+ accuracy transcription and GPT-4o-mini for optional AI enhancement (grammar correction, style rewriting, translation). Unlike most voice dictation tools that require users to provide their own OpenAI API key, LinguaVox includes a shared key pool — free users get 20 requests per day with zero setup. Power users and teams can bring their own key for unlimited usage.

## How It Works

**Before LinguaVox:** open a separate app → record → copy → switch to browser → paste  
**After LinguaVox:**

```
1. Click any web field (Slack, Gmail, Notion, Jira…)
2. Hold  Ctrl+Space  →  speak
3. Release  →  text appears within ~3 seconds  ✓
```

No copy-paste. No switching apps. Works on any website.

## Browser & OS Requirements

| Browser | Status | Notes |
|---------|--------|-------|
| Chrome 88+ | ✅ | Fully supported |
| Edge (Chromium) | ✅ | Should work — same Chromium APIs, not officially tested |
| Brave | ✅ | Should work — not officially tested |
| Opera | ✅ | Should work — not officially tested |
| Firefox | ❌ | Not supported — different extension API |

**OS:** Windows, macOS, Linux — anywhere Chrome/Edge/Brave runs.  
**Google Account required** — free tier login uses Google OAuth. No Google account = no free tier (BYOK still works without Google sign-in is not yet supported).

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


All OpenAI API calls go through the Worker. API keys never leave the server.

## Key Features

- **No API key required** — 20 req/day free via shared pool, zero setup
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

| Plan | Requests/day | Requirements |
|------|-------------|--------------|
| Free | 20 | Google Account (OAuth login) |
| Bring Your Own Key | Unlimited | Google Account + your OpenAI API key |
| Organization | Unlimited | Google Account + shared team API key |

## FAQ

### Does LinguaVox work on Slack?
Yes. Slack intercepts keyboard events at the page level. LinguaVox registers the hotkey at the browser level via `chrome.commands.onCommand`, bypassing Slack's capture. Works in all Slack message fields.

### Do I need an OpenAI API key?
No. Free users get 20 requests/day from the shared pool. Add your own key in the dashboard for unlimited usage.

### Is my voice recorded or stored?
No. Audio is processed in real-time by Whisper and discarded immediately. Zero voice data retained anywhere.

### What languages are supported?
21+ languages: English, Ukrainian, Russian, Spanish, French, German, Japanese, Korean, Chinese, Arabic, Portuguese, Italian, Polish, Dutch, Turkish, Swedish, Romanian, Greek, Tagalog, Urdu, Punjabi, and more.

## Documentation

| Resource | Description |
|----------|-------------|
| [Use Cases](docs/use-cases.md) | Customer support, devs, non-native speakers, RSI |
| [Integrations](docs/integrations.md) | Platform-specific notes for Slack, Notion, Jira, etc. |
| [Security & Data Protection](docs/security.md) | How API keys, audio, and personal data are handled |
| [FAQ](docs/faq.md) | 20+ answers |
| [Changelog](docs/changelog.md) | v1.0 → v2.8 |

## Installation

1. [Chrome Web Store →](https://chromewebstore.google.com/detail/linguavox/TODO) — click "Add to Chrome"
2. Click the LinguaVox icon → "Sign in with Google"
3. Press Ctrl+Space anywhere and start speaking

**For Bring Your Own Key:** [Dashboard → API Key](https://linguavox-landing.pages.dev/dashboard/apikey)

## Links

| | |
|--|--|
| 🌐 Website | https://linguavox-landing.pages.dev |
| 📊 Dashboard | https://linguavox-landing.pages.dev/login |
| 🔒 Privacy Policy | https://linguavox-landing.pages.dev/privacy/ |
| 🤖 AI docs (llms.txt) | https://linguavox-landing.pages.dev/llms.txt |
| 💬 Support | https://linguavox-landing.pages.dev/support/ |

## License

MIT — see [LICENSE](LICENSE)
