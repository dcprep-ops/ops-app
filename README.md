# DC Prep Operations App

A mobile web app for the DC Prep operations team. Staff use it to log drills, complete common space walkthroughs, and access other operational tools — all from a single link saved to their phone's home screen.

## What's in this repo

| File | What it is |
|------|-----------|
| `index.html` | The entire app — one self-contained file |
| `README.md` | This file |

## How to update the app

1. Go to [github.com](https://github.com) and sign in
2. Click on `index.html` in the file list
3. Click the **pencil icon** (Edit this file) in the top right
4. Make your changes
5. Click **Commit changes** at the bottom

The live app updates within about 60 seconds. No action needed from staff.

If you want to replace the whole file at once (e.g. a major new version), click **Add file → Upload files** and drag the new `index.html` in. It will overwrite the old one.

## How staff access the app

Share this link with staff: `https://[your-github-username].github.io/[repo-name]/`

They open it in their phone browser and tap **Add to Home Screen** to save it as an app icon. After that they tap the icon like any other app — no link needed.

## Active tools

| Tool | Who uses it | What it captures |
|------|------------|-----------------|
| Evacuation & Lockdown Drill | OSL (official record), all staff (observations) | Drill type, timing, observations, compliance data |
| Common Space Walkthrough | OSL, Principal, SDO, Other | Room-by-room checklist across 11 space types |
| Ops AI Bingo | All staff (fixed list of 9 names, closed contest) | Which of 25 AI-use squares each person has marked, Sept 1–21 |

## Tools in preview (coming soon)

- Arrival & Dismissal Observation
- Building Walkthroughs
- Security Patrol Log
- Log Daily Attendance Check

## Where data goes

Submissions write live to a Google Sheet ("DC Prep Ops App Log") via a Google Apps Script Web App. The URL is set as `SCRIPT_URL` near the bottom of `index.html`.

Most tools append a new row per submission. Ops AI Bingo is the exception: each person has one row that gets updated in place every time they mark or unmark a square, rather than a new row per action. See `bingo-appsscript-addition.gs` for that handler if you need to modify it — it's structured differently from the rest of the Apps Script project for that reason.

Contact the initiative owner or the DC Prep data team for access to the underlying Sheet or Apps Script project.

## Questions or issues

If something in the app looks broken or needs to change, the fastest path is to open `index.html`, find the relevant section, and edit the text or logic directly. The file is organized with clearly labeled comments for each screen and flow.
