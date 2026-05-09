# LinguaVox Changelog

## v2.8 — Dashboard + Bring Your Own Key + Org Management

- **Web Dashboard** at `linguavox.uk/dashboard/`
- **Bring Your Own Key** — connect personal OpenAI API key for unlimited usage
- **Organization accounts** — create a team, share API key pool, view member usage analytics
- **Org management** — invite/remove members, owner-level access control
- **Usage analytics** — today's request count + 7-day chart in dashboard overview
- Rate limit: 20 requests/day on shared API key pool (unlimited with BYOK)

## v2.8 — Landing Page + Privacy Policy

- New marketing landing page with pricing section and 3-step onboarding
- Privacy policy page
- Chrome Web Store listing prepared

## v2.7 — AI Enhancement Modes

- 6 AI enhancement modes: Smart Polish, Business Style, Grammar Fix, Creative Style, Casual Style, Academic Style
- Enhancement uses Chat Completions (GPT-4o-mini), not Assistants API
- Try/catch fallback: original transcription preserved if enhancement fails

## v2.6 — Translation Mode

- Speak in any language, get output in any target language
- Translation via GPT-4o-mini after Whisper transcription
- Target language selector in popup

## v2.5 — Multi-language Support

- 21+ languages for transcription
- Language auto-detection option
- Interface localization for 14+ locales

## v2.0 — Cloudflare Worker Backend

- All OpenAI calls moved to Cloudflare Worker — API keys never leave the server
- Google OAuth authentication
- JWT-based session management
- Rate limiting via Cloudflare KV

## v1.0 — Initial Release

- Voice transcription via OpenAI Whisper
- Ctrl+Space hotkey (hold to talk)
- Text insertion into any web input field
- React/Draft.js/Quill compatible text insertion
- Slack support via `chrome.commands.onCommand`