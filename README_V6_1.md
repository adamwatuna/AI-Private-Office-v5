# AI Private Office V6.1 — Staff Character Builder

- Each virtual office staff card has a **Manage Config** shortcut.
- Also available under **My Staff**, staff profile and V5 Hiring.
- Set personality, communication style, working style, decision approach, skills, CEO custom instructions, restrictions, autonomy preference and memory notes.
- **Save Character Config** stores preferences in this browser's localStorage, alongside existing staff/task demo data. This is not secure server-side persistence and does not sync between devices.
- The V6 AI draft generator receives the selected staff's character configuration and uses it to shape drafts. Existing tasks can be re-drafted with current staff preferences.
- **No autonomous actions, permissions, real tool integrations or external publishing are enabled.** The autonomy selector is only a preference. All drafts require CEO review.
- Do not enter secrets, private client data, or sensitive information in character notes while the app is a development starter.
- Deploy via existing Dockerfile and Railway environment variables. Keep .env private.
