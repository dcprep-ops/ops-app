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

## Tools in preview (coming soon)

- Arrival & Dismissal Observation
- Building Walkthroughs
- Security Patrol Log
- Log Daily Attendance Check

## Where data goes

Currently, submissions display a confirmation screen but do not yet write to a database. To connect live data storage, a Google Apps Script Web App URL needs to be added to the `fetch()` call near the bottom of `index.html`. The script should accept a POST request and append a row to a Google Sheet.

Contact the initiative owner or the DC Prep data team to set this up.

## Questions or issues

If something in the app looks broken or needs to change, the fastest path is to open `index.html`, find the relevant section, and edit the text or logic directly. The file is organized with clearly labeled comments for each screen and flow.
