# BCBA Assistant

A clinical support tool built for a Board Certified Behavior Analyst (BCBA). Helps streamline the creation of behavior intervention plans, RBT program sheets, parent training materials, and session documentation.

Built as a single-file web app — no installation required. Open in any browser.

---

## Features

- **Dashboard** — All-clients overview with monitoring alerts and at-a-glance stats
- **BIP Generator** — AI-assisted Behavior Intervention Plan drafts following company template structure (operational definition, onset/offset, function, antecedents, reinforcers, proactive and reactive strategies)
- **RBT Program Sheet Generator** — Generates target descriptions in the exact field format used by the clinical team (SD, prompting strategies, error correction, reinforcement, etc.)
- **Parent Training** — Three tools: pre-meeting agenda, during-meeting guide (follows session flow), and printable parent handout
- **I'm Stuck** — Conversational AI clinical brainstorm for when you're stumped on a behavior or goal. Remembers context across the conversation.
- **Note Templates** — Reusable session note phrases for Central Reach. Multi-select and copy as a block.
- **Client Profiles** — Per-client storage of goals (with sub-goals), active/mastered/discontinued targets, monitoring schedule with overdue alerts, parent meeting log, and session notes
- **Speech-to-Text** — Dictation support on all major input fields
- **Password Login** — Single shared password with session persistence. Changeable from the sidebar.
- **Print / PDF** — Clean print output for BIPs, RBT program sheets, and parent handouts

---

## Tech Stack

- Pure HTML / CSS / JavaScript — no frameworks, no build step, no dependencies
- All client data stored in `localStorage` (browser only — nothing sent to any server)
- AI features powered by the [Anthropic Claude API](https://console.anthropic.com) (requires your own API key)
- Hosted via [GitHub Pages](https://pages.github.com)

---

## Setup

### 1. API Key
An Anthropic API key is required for all AI generation features.
- Get one at [console.anthropic.com](https://console.anthropic.com) → API Keys
- Enter it in the app via **API Key Settings** in the sidebar
- The key is stored in your browser only and sent directly to Anthropic — never to any other server

### 2. Password
Default password on first launch: `bcba2024`
Change it immediately via **Change Password** in the sidebar.

### 3. Hosting
This app is hosted via GitHub Pages at:
`https://dazat.github.io/bcba-assistant`

---

## Updating the App - By developer & Claude Code

-- Via Github uploads

---

## Data & Privacy

- All client data is stored in the browser's `localStorage` on the device being used
- Data does **not** sync between devices automatically
- No client data is sent to any external server
- Client names are stored as initials only (e.g. `JaDo` for Jane Doe)
- AI generation sends only the text entered into each form field to Anthropic's API — no stored client data is sent automatically
- The app does not collect analytics or usage data of any kind

---

## Known Limitations

- Data is device-specific — entering data on a phone will not appear on a laptop and vice versa
- Password protection is client-side only — sufficient for casual privacy, not a substitute for HIPAA-compliant storage
- This tool is a clinical aid only — all AI-generated content must be reviewed and edited by the BCBA before use
- Speech-to-text requires Chrome or Safari

---

## Bug Log & Feature Requests

Bugs and feature requests are tracked in the [Issues tab](../../issues) of this repository.

See current open items there. To add a new one:
1. Click **Issues** → **New Issue**
2. Use the label `bug` for broken functionality or `enhancement` for new features
3. Describe what happened, what you expected, and which version you were using

---

## Version History

| Version | Notes |
|---------|-------|
| v1 | Initial build — basic notes, behavior plan, parent training, BT comms |
| v2 | Full rebuild — client profiles, BIP generator, RBT program sheets, parent training tabs, I'm Stuck chat, note templates, speech-to-text, monitoring schedule |
| v3 | Editable goals/templates, multi-select templates, larger text, Nunito/Quicksand fonts, dashboard overview, BT comms removed |
| v4 | Copy bug fix (notes + templates), password login screen, Change Password + Lock App in sidebar |

---

## Built With

Designed and developed with [Claude](https://claude.ai) by Anthropic.
