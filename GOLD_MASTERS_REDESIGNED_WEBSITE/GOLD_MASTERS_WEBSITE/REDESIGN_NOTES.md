# Gold Masters frontend redesign — handoff notes

## Included
- `index.html`: simplified navigation, home dashboard, AI brief presentation and account entry points.
- `style.css`: newly supplied primary stylesheet (the uploaded archive did not contain the original `style.css`).
- `mobile.css`: responsive/mobile refinements.
- `logo.png` and `logo.svg`: temporary Gold Masters monogram assets created for this redesign. Replace with the official logo if you have it.
- Existing `app.js`, `app.py`, requirements, PWA files and icons are retained from the supplied archive.

## Important implementation boundaries
- The existing backend and API contracts were not rewritten.
- The existing AI endpoint returns an AI/rule-based market brief; no conversational chat endpoint was present in the supplied frontend/backend. The new page labels this accurately rather than pretending a chat feature exists.
- AUTO/MANUAL controls are no longer presented as clickable switches in this simplified customer interface. Existing mode status fields are retained for compatibility. The Connect page's legacy broker-operation controls are hidden from the new beginner-facing UI. This is a frontend presentation change, not a backend security control and does not stop an already-running EA or disable server endpoints.
- Before any production deployment, the site owner should have an appropriately authorized adult review account permissions, broker integrations, payment flows, applicable laws and the server-side authorization rules. Do not treat hidden frontend controls as access control.
- The archive originally included private `.mq5` EA source files. Those files are intentionally excluded from this website deployment ZIP. Keep owner/customer EA source files private and never upload them to a public website repository.

## Deploy
1. Back up the current website repository and production deployment.
2. Review the changed `index.html`, `style.css`, `mobile.css` and `sw.js` in a staging environment.
3. Confirm API base URL and required Render environment variables are correct.
4. Test login, registration, AI brief, market data, news, account pages and responsive layouts with test accounts.
5. Deploy only after an authorized site administrator approves the staging test.

## Known limitations
- The original official `style.css`, `logo.png`, `logo.svg` and `intro.mp4` were not present in the uploaded ZIP. A replacement stylesheet and temporary monogram logo are included; no intro video was recreated.
- A true conversational AI assistant requires a dedicated backend chat endpoint and provider configuration. This deliverable improves the existing AI brief UX but does not invent that backend capability.
