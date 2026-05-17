# Reputifly Revision Pack v3

Lives at **https://revise.reputifly.cloud**

## URLs

- **Client editor**: `https://revise.reputifly.cloud/?token={TOKEN}` — receive a token via revision link email, click, edit
- **Staff admin**: `https://revise.reputifly.cloud/admin` — staff-auth gated. Drop a client's Archimedes agent profile, pick pages, generate a revision link
- **Test runner**: `https://revise.reputifly.cloud/pack-tests` — 40 unit tests for the pack pipeline

## What this serves

The unified Reputifly revision flow:
1. Client clicks the revision link → opens v2 editor with their pages
2. Client edits text/images, right-click sections to comment
3. Client clicks "Notify Completion" → backend builds a structured v3 revision pack ZIP
4. Pack uploaded to Firebase Storage; staff emailed + Firestore `pending_revisions` doc written
5. Staff hands the pack URL + the site's agentic-JSON profile to Claude Code → applies revisions
