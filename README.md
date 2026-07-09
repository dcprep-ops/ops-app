# DC Prep Operations App

A mobile web app for the DC Prep operations team. Staff use it to log drills, complete walkthroughs, submit observations, and access other operational tools — all from a single link saved to their phone's home screen.

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
| Evacuation & Lockdown Drill | OSL, Principal, COO, SDO, Other | Drill type, timing, compliance data, observer notes |
| Common Space Walkthrough | OSL, Principal, COO, SDO, Other | Space-by-space checklist across 10 spaces; flags and notes per space |
| Arrival & Dismissal Observation | OSL, Principal, COO, SDO, Other | 10-item checklist, overall rating, period (arrival/dismissal), notes |
| Custodial Walkthrough | Director of Facilities, Facilities Team, Custodial Vendor | Three walk types: DoF Bi-Weekly, Facilities Team Weekly (space-by-space), Monthly with Vendor |
| Create Facilities Request | All staff | Routes to the Google Form for the selected campus cluster |
| BOY Classroom Readiness | Principal, OSL, COO, MD of Schools, SDO, Other | Room-by-room readiness assessment with grade-band checklists |

## Tools in preview (coming soon)

- Request Tech Support
- Security Patrol Log
- Log Daily Attendance Check

## Where data goes

Submissions are sent to a Google Sheet via a Google Apps Script web app. Each flow has its own tab in the sheet:

| Sheet tab | Flow |
|-----------|------|
| Drill Log | Evacuation & Lockdown Drill |
| Common Space Walkthrough | Common Space Walkthrough |
| Arrival Dismissal | Arrival & Dismissal Observation |
| Custodial Walkthrough | Custodial Walkthrough |
| Classroom Readiness | BOY Classroom Readiness |

The Apps Script URL is embedded in `index.html`. To update it, search for `SCRIPT_URL` near the top of the script block and replace the value.

## Data structure

All checklist flows use a `Space — Item` column naming convention (e.g. `Lobby — Furniture is inviting and in good condition`). This makes it easy to filter and analyze by space in Google Sheets.

Items are stored as `checked`, `flagged`, `skipped`, or `no input`.

## Companion tools

| Tool | Purpose |
|------|---------|
| Ops Dashboard | Live view of drills, arrival/dismissal, and custodial data |
| BOY Readiness Dashboard | Classroom readiness by school and status |
| Walkthrough Triage Tool | OSL reviews flags, assigns owners, generates follow-up emails |

## Questions or issues

If something in the app looks broken or needs to change, the fastest path is to open `index.html`, find the relevant section (each flow has clearly labeled comments), and edit directly.

For larger changes, contact the initiative owner. The app is built as a single self-contained HTML file — no build tools or dependencies required.
