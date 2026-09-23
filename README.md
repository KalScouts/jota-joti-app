# Kalgoorlie Scout Group — JOTA-JOTI 2026 Full Deploy Kit

This kit is split into two parts so the public GitHub Pages site does not expose the private Apps Script source or spreadsheet data.

## Public site
Repository: `https://github.com/KalScouts/jota-joti-app`
Expected GitHub Pages URL: `https://kalscouts.github.io/jota-joti-app/`

Upload **only the contents of `GitHub-Pages/`** to the root of the public repository.

The public site is wired to:
- Apps Script web app: `https://script.google.com/macros/s/AKfycbyIHdl2mm2LzxCIndnlN3AAaxaB0sC1XxTjub487xZuYUF3ad9vU0eG1KFIeFMdlpuY/exec`
- Google Form: `https://docs.google.com/forms/d/e/1FAIpQLSevs4K7aNGjPOSBk9tjFZtShpqkRQUAOjVetaInhpaaOARFrA/viewform?usp=header`

## Google Sheet / Apps Script
1. Import `Google-Sheets/Kalgoorlie_Scout_Group_JOTA_JOTI_Template.xlsx` into Google Sheets, or use it as the structure for the sheet linked to the form.
2. Link your Google Form to this new Google Sheet.
3. Open **Extensions → Apps Script** from THIS Sheet.
4. Paste `Google-Sheets/Kalgoorlie_Scout_Group_JOTA_JOTI_AppsScript.gs`.
5. Save and authorise it.
6. Run `setupEOISystem()` once from the `JOTA-JOTI Admin` spreadsheet menu.
7. Confirm the `onFormSubmit` installable trigger exists.
8. Deploy the Apps Script as a Web App with the access setting needed for the public dashboard. The public site expects the deployed URL shown above. If you create a new deployment URL, update `site-config.js`, `script.js`, and `admin.js` before publishing.

## Important
- Do NOT upload `Google-Sheets/` to the public GitHub repository.
- Do NOT expose the `Users` sheet publicly.
- The live Apps Script URL supplied by the project owner could not be independently health-checked from this environment because the endpoint timed out; the site is nevertheless configured to use that exact URL.
- The new backend source has the spreadsheet ID left blank so a container-bound Apps Script can use its own Google Sheet. This keeps the new group independent from the old spreadsheet.

## Site routes
- `/` main countdown/dashboard
- `/setup` parent setup guide
- `/skip` test/preview page
- `/track` JID tracker
- `/admin@5-6-4-3` secret admin route

## Creator credit
Made by Hunter Miller from Boulder Scout Hall.
