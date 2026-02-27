# BCBA Assistant

A clinical support tool built for a Board Certified Behavior Analyst (BCBA). Helps streamline the creation of behavior intervention plans, RBT program sheets, parent training materials, and session documentation.

Built as a single-file web app — no installation required. Open in any browser.

---

## Features

- **Dashboard** — All-clients overview with monitoring alerts and at-a-glance stats
- **BIP Generator** — AI-assisted Behavior Intervention Plan drafts following company template structure (operational definition, onset/offset, function, antecedents, reinforcers, proactive and reactive strategies). Per-section copy buttons and a one-click Copy for Central Reach button.
- **RBT Program Sheet Generator** — Generates target descriptions in the exact field format used by the clinical team (SD, prompting strategies, error correction, reinforcement, etc.). Each field has its own copy button for direct paste into Central Reach.
- **Parent Training** — Three tools: pre-meeting agenda, during-meeting guide (follows session flow), and printable parent handout
- **I'm Stuck** — Conversational AI clinical brainstorm for when you're stumped on a behavior or goal. Remembers context across the conversation.
- **Note Templates** — Reusable session note phrases for Central Reach. Multi-select and copy as a block. Editable in place.
- **Client Profiles** — Per-client storage of goals (with editable sub-goals), active/mastered/discontinued targets, monitoring schedule with overdue alerts, parent meeting log, and session notes
- **Document Import** — Upload a PDF or image of a clinical document (assessment, IEP, CR export) and the AI extracts goals and targets automatically. Review and edit before saving.
- **Speech-to-Text** — Dictation support on all major input fields
- **Password Login** — Single shared password with session persistence. Changeable from the sidebar.
- **Export / Import** — Download a full data backup as a JSON file. Restore from any previous backup. Weekly reminder if backup is overdue.
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

## Updating the App — By developer & Claude Code

-- Via GitHub uploads

---

## Data & Privacy

- All client data is stored in the browser's `localStorage` on the device being used
- Data does **not** sync between devices automatically
- No client data is sent to any external server
- Client names are stored as initials only (e.g. `JaDo` for Jane Doe)
- AI generation sends only the text entered into each form field to Anthropic's API — no stored client data is sent automatically
- Document uploads (PDF/image) send document content to Anthropic's API for reading — use documents with initials only where possible
- The app does not collect analytics or usage data of any kind

---

## Data Backup

Client data lives in the browser and can be cleared by browser updates, cache clears, or switching devices. To protect against data loss:

- Use **Export Data Backup** in the sidebar regularly to download a `.json` backup file
- Save backup files to iCloud Drive or another safe location accessible from all devices
- Use **Import Data Backup** to restore from any previous backup, or to migrate data to a new device
- The app will remind you to back up if 7 or more days have passed since your last export

---

## Known Limitations

- Data is device-specific — entering data on a phone will not appear on a laptop and vice versa
- Password protection is client-side only — sufficient for casual privacy, not a substitute for HIPAA-compliant storage
- This tool is a clinical aid only — all AI-generated content must be reviewed and edited by the BCBA before use
- Speech-to-text requires Chrome or Safari
- Document import works best with clean PDF exports — photo quality affects extraction accuracy

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
| v0 | Initial build — basic notes, behavior plan, parent training, BT comms |
| v0.1 | Full rebuild — client profiles, BIP generator, RBT program sheets, parent training tabs, I'm Stuck chat, note templates, speech-to-text, monitoring schedule |
| v0.2 | Editable goals/templates, multi-select templates, larger text, Nunito/Quicksand fonts, dashboard overview, BT comms removed |
| v1 | Copy bug fix (notes + templates), password login screen, Change Password + Lock App in sidebar |
| v2 | Export/import data backup, weekly backup reminder banner, auto-fill client initials on generator pages |
| v3 | Document upload (PDF/image → auto-extract goals & targets with review screen), per-section copy on BIP, Copy for Central Reach on BIP and RBT, RBT field-by-field copy buttons |
| v3.1 | Fixed Add Client box appearance |
| v3.2 | Added monitoring functionality to use UX inputs of Targets and Goals as a dropdown |

---

## Built With

Designed and developed with [Claude](https://claude.ai) by Anthropic.
