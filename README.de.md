<p align="center">
  <a href="README.md">English</a> · <a href="README.uk.md">Українська</a> · <a href="README.ru.md">Русский</a> · <a href="README.zh-CN.md">中文</a> · <a href="README.es.md">Español</a> · <a href="README.de.md">Deutsch</a> · <a href="README.ja.md">日本語</a>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/kos-4862/linguavox-public/main/images/banner.png" width="800" alt="LinguaVox — KI-Sprachdiktat Chrome-Erweiterung" />
</p>

<h3 align="center">LinguaVox — KI-Sprachdiktat Chrome-Erweiterung</h3>

<p align="center">
  Tastenkombination halten · sprechen · loslassen · Text erscheint in 3 Sekunden in jedem Webfeld<br>
  OpenAI Whisper · 21+ Sprachen · Kein API-Schlüssel · Slack, Gmail, Notion, Jira
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/Lizenz-MIT-blue.svg" alt="Lizenz" /></a>
  <a href="https://linguavox-landing.pages.dev"><img src="https://img.shields.io/badge/Website-linguavox-brightgreen" alt="Website" /></a>
  <a href="https://chromewebstore.google.com/detail/linguavox/TODO"><img src="https://img.shields.io/badge/Chrome%20Web%20Store-Kostenlos%20installieren-blue?logo=googlechrome" alt="Chrome Web Store" /></a>
  <a href="https://linguavox-landing.pages.dev/dashboard/"><img src="https://img.shields.io/badge/Dashboard-öffnen-orange" alt="Dashboard" /></a>
  <img src="https://img.shields.io/badge/Version-2.8-green" alt="Version" />
</p>

---

## Was ist LinguaVox?

LinguaVox ist eine Chrome-Erweiterung für KI-gestütztes Sprachdiktat und Übersetzung. Halte Ctrl+Space gedrückt, sprich, lass los — und der transkribierte Text erscheint sofort im aktiven Textfeld: Chat-Boxen, E-Mail-Editoren, Suchfelder, CRM-Formulare und Code-Editoren. Die Erweiterung nutzt OpenAI Whisper für 95%+ Genauigkeit und GPT-4o-mini für optionale KI-Verbesserung: Grammatikkorrektur, Stilumschreibung, Übersetzung.

Anders als die meisten Diktierwerkzeuge benötigt LinguaVox keinen eigenen OpenAI-API-Schlüssel. Kostenlose Nutzer erhalten 100 Anfragen täglich aus einem gemeinsamen Schlüsselpool — ohne jede Einrichtung. Power-User und Teams können ihren eigenen Schlüssel für unbegrenzte Nutzung einbinden.

## Wie es funktioniert

**Vorher:** Separate App öffnen → aufnehmen → kopieren → Tab wechseln → einfügen  
**Mit LinguaVox:**

```
1. In ein beliebiges Feld klicken (Slack, Gmail, Notion, Jira…)
2. Ctrl+Space  halten  →  sprechen
3. Loslassen  →  Text erscheint in ~3 Sekunden  ✓
```

Kein Kopieren. Kein App-Wechsel. Auf jeder Website.

## Wo es funktioniert

| Plattform | Status | Hinweise |
|-----------|--------|----------|
| Slack (Browser) | ✅ | Browser-Level-Hotkey umgeht Slacks Tastaturerfassung |
| Gmail | ✅ | Schreib- und Antwortfelder |
| Notion | ✅ | Alle `contenteditable`-Blöcke |
| Jira | ✅ | Aufgabenfelder, Kommentare, Beschreibungen |
| Asana | ✅ | Aufgaben- und Kommentarfelder |
| Salesforce | ✅ | CRM-Eingabefelder |
| Jedes `<input>` / `<textarea>` | ✅ | Universal — jede Website |
| Jedes `contenteditable` | ✅ | React, Draft.js, Quill kompatibel |
| Google Docs | ⚠️ | Eingeschränkt — benutzerdefinierter Canvas-Editor |

## Hauptfunktionen

- **Kein API-Schlüssel** — 100 Anfragen/Tag kostenlos aus gemeinsamem Pool, null Einrichtungsaufwand
- **Eigener Schlüssel (BYOK)** — unbegrenzte Nutzung zu OpenAI-Kosten (~$0,50/Monat)
- **Organisations-Konten** — gemeinsamer Schlüsselpool, Mitgliederverwaltung, Nutzungsanalysen
- **21+ Sprachen** — Transkription und Übersetzung in einem Schritt
- **6 KI-Verbesserungsmodi** — Grammatikkorrektur, Business-Stil, Akademisch, Casual, Kreativ, Smart-Polish
- **Datenschutz** — Audio wird nie gespeichert, Echtzeit-Verarbeitung und sofortiges Verwerfen
- **Unter 3 Sekunden** — von Sprache bis eingefügtem Text Ende-zu-Ende
- **95%+ Genauigkeit** — OpenAI Whisper large-v2

## KI-Verbesserungsmodi

| Modus | Funktion |
|-------|----------|
| Smart Polish | Grammatik korrigieren, Klarheit verbessern, Bedeutung erhalten |
| Business-Stil | Für professionelle Kommunikation umschreiben |
| Grammatikkorrektur | Nur Grammatik und Rechtschreibung |
| Kreativer Stil | Lebhafter, ansprechender Text |
| Casual-Stil | Freundlicher, gesprächiger Ton |
| Akademischer Stil | Formelle akademische Sprache |

## Preise

| Plan | Anfragen | Einrichtung |
|------|----------|-------------|
| Kostenlos | 100/Tag | Nur Google-Anmeldung |
| Eigener Schlüssel | Unbegrenzt | Dein OpenAI API-Schlüssel |
| Organisation | Unbegrenzt | Gemeinsamer Team-Schlüssel + Analysen |

## Häufige Fragen

### Funktioniert LinguaVox in Slack?
Ja. Slack fängt Tastaturereignisse auf Seitenebene ab. LinguaVox registriert den Hotkey auf Browser-Ebene über `chrome.commands.onCommand` und umgeht damit Slacks Erfassung. Funktioniert in allen Slack-Nachrichtenfeldern.

### Brauche ich einen OpenAI API-Schlüssel?
Nein. Kostenlose Nutzer erhalten 100 Anfragen/Tag aus dem gemeinsamen Pool. Eigenen Schlüssel im Dashboard hinzufügen für unbegrenzte Nutzung.

### Wird meine Stimme aufgezeichnet oder gespeichert?
Nein. Audio wird von Whisper in Echtzeit verarbeitet und sofort verworfen. Keine Sprachdaten werden irgendwo gespeichert.

## Links

| | |
|--|--|
| 🌐 Website | https://linguavox-landing.pages.dev |
| 📊 Dashboard | https://linguavox-landing.pages.dev/dashboard/ |
| 🔒 Datenschutzerklärung | https://linguavox-landing.pages.dev/privacy/ |
| 💬 Support | https://linguavox-landing.pages.dev/support/ |

## Lizenz

MIT — siehe [LICENSE](LICENSE)