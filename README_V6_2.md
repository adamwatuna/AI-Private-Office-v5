# AI Private Office V6.2 — CEO Walkthrough & Command Centre

This update preserves the original V2 office background and six desk coordinates and retains V6.1 Manage Config and AI draft generation.

## Implemented
- Click staff desks to open CEO Walkthrough with previous/next desk navigation.
- Each desk shows assigned tasks, draft-review queue, CEO-entered progress, and quick actions for task assignment, staff profile, and character config.
- Executive Briefing summarises saved task counts, overdue assignments, and approvals.
- CEO Approval Desk links to existing draft review and approval workflow.
- Only an *in-flight* OpenAI draft request is marked "AI processing"; no fabricated activity or fake progress.
- Removes hard-coded sample activity from the original office page.

## Not yet implemented
- True background agent jobs, durable run state, automatic progress calculation, real-time multi-device updates, shared memory, external integrations, production security, and real autonomous boardroom meetings. Existing V5 modules remain demo UIs.
- Staff/task/config data are stored in the current browser's localStorage; backend draft generation requires CEO login. This is not a secure shared enterprise database.

## Railway / GitHub
Upload the extracted project files **inside the same existing project folder path** used by the currently successful Railway deployment. Do not create another nested ZIP folder. Keep Railway Root Directory unchanged if the repository structure stays unchanged. Do not commit `.env`; set secrets in Railway Variables.

## Security
Do not use with confidential organisational data or external partner accounts until secure auth, server-side permissions, encrypted durable storage, audit logging and backup policies are implemented.
