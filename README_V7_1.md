# V7.1 — Interactive Desk Occupancy

Built on the uploaded V7 Executive Headquarters source. Original office-background.png retained.

- Six mapped desks in the original office image show OCCUPIED when assigned and VACANT when empty.
- Clicking a vacant desk opens Manage AI Staff. New staff fill the lowest vacant seat.
- Clicking an occupied desk opens the existing CEO Walkthrough; Manage Config remains available.
- Vacate Desk removes the staff profile only if they have no assigned tasks, with confirmation. Export a V7 backup first.
- More than six staff are shown in a clearly labelled Expansion Workstations panel, not misleadingly overlaid on desks that do not exist in the image.
- Occupancy is derived from browser-local staff records, not actual online presence. AI processing indicators still reflect only in-flight requests in the current browser session.
- Browser-local storage, login and authorization limitations from V7 still apply. Not production-ready.

Deployment: extract and upload the contents to the same GitHub source folder that Railway builds; do not upload .env.
