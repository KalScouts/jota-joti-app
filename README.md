# JOTA-JOTI Dashboard - Kalgoolie Scout Group

Unofficial JOTA-JOTI 2026 website and account system for Kalgoolie Scout Group.

- Site: https://kalscouts.github.io/
- Backend: Google Apps Script (`Code.gs`) reading the live Google Sheet (ID set in `CONFIG.SPREADSHEET_ID`)
- Contact / reply-to: jotajoti.kalgoolie@gmail.com

## Deploying
1. Paste `Code.gs` into the Apps Script project, signed in as jotajoti.kalgoolie@gmail.com.
2. Run `setupEOISystem` once (creates sheets, headers and triggers).
3. Deploy > Web app (Execute as: Me, Access: Anyone). The URL must match `config.js` and `script.js`.
4. Upload the section forms to the repo root: `Kalgoolie-Joey-Section-Form.pdf`, `Kalgoolie-Cub-Section-Form.pdf`, `Kalgoolie-Scout-Section-Form.pdf`, `Kalgoolie-Venturer-Section-Form.pdf`.
5. Add event dates/times in `setup.html` (search for ADD EVENT DATES).
6. Manage accounts and send bulk email from the **JOTA-JOTI Admin** menu inside the Google Sheet (there is no web admin page).
7. After every website change, bump `APP_VERSION` in `sw.js`.

Made by Hunter Miller from Boulder Scout Hall.
