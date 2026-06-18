# Newsdesk Roster

Read-only weekly duty roster for the EBS news desk. People-first cards, a timeline, and a weekly board. Updates itself for 7–8 viewers when you publish a new week.

## Your weekly routine (one upload)
1. Fill the Excel (set the **WEEK STARTING** Monday date on the READ ME tab, statuses, then the grid).
2. In the repo: Add file → Upload files → drop the filled file in, **named `roster.xlsx`**, commit.
3. A GitHub Action converts it to `roster.json` automatically and republishes. Done.
4. The 7–8 colleagues just open their bookmark; they see the new week on next open. No installs, no accounts.

## Files
- `index.html` — the reader (cards / timeline / week views)
- `roster.xlsx` — the week you fill and upload
- `convert.py` — turns the Excel into `roster.json` (run by the Action)
- `roster.json` — the published data the app reads
- `.github/workflows/publish.yml` — runs the conversion on every `roster.xlsx` upload

## Setup (once)
1. New public repo, push these files.
2. Settings → Pages → deploy from `main`, root.
3. Open the Pages URL, add to home screen, share the link with the team.

Stable for many simultaneous viewers: it's a static read-only page, so "8 people at once" is trivial.
