# AI Private Office V7 — Executive Headquarters (development release)

Based on V6.2. Preserves original office-background.png and desk coordinates.

## Implemented and usable
- V6.1 staff Character Builder / Manage Config, preferences passed to AI draft generator
- V6.2 clickable desks, CEO Walkthrough, task records, draft review and CEO approvals
- V7 Executive HQ summarizing browser task records
- V7 AI Boardroom: **one OpenAI call** synthesizing role-specific perspectives and minutes for CEO review; not separate autonomous AI agents
- V7 AI Executive Briefing: OpenAI summary of current browser task records
- V7 Knowledge Library: browser-only reference notes; **not** connected to AI retrieval
- V7 Staff Messenger: browser-only notes; **not** messages sent to autonomous staff
- V7 staff task performance summaries
- V7 governance policy notes, manual JSON export/import of local records
- Existing backend CEO-password-protected AI draft and AI executive endpoints

## Not implemented / production limitations
- No autonomous or continuously working staff, multi-agent orchestration, background jobs, automatic staff-to-staff workflows, live cross-device status, real-time notifications, secure multiuser permissions, MFA, third-party integrations, secure vault, or audit-grade logging.
- Task progress and activity reflect local browser records and CEO updates. V7 notes, meetings, messages, staff and tasks are browser-local. Backend `/api/snapshot` exists but is not automatically synced with these frontend records.
- Do not use for confidential records, partners or production operations until proper authorization, persistence, backups and security review are implemented.
- No automatic email, publishing, payments, or external actions.

## Deployment
1. Extract ZIP. Keep `frontend/`, `backend/`, `Dockerfile`, `requirements.txt` at the same level.
2. Replace these files in the **same GitHub folder** that Railway currently builds. Do not upload the ZIP itself and do not nest another V7 folder.
3. Keep Railway Root Directory pointing to that existing folder. Dockerfile path `Dockerfile`. Watch Paths blank.
4. Keep `OPENAI_API_KEY`, `CEO_PASSWORD`, `SESSION_SECRET` only in Railway Variables. Never upload `.env`.
5. Configure a Railway volume mounted at `/app/data` for backend file/database persistence if using SQLite; a managed database is preferable for production.
6. After deploy, verify `/api/health`, then use V7 Executive HQ from the sidebar. AI Boardroom/Briefing will prompt for backend CEO password.

## Security notes
- The V7 JSON backup includes staff profiles, tasks, notes and meeting minutes. Protect it like a private document.
- The AI Boardroom passes selected staff descriptions and configurations to the OpenAI API. Do not enter secrets into those fields.
