# Contact form → daily log (Google Sheets, no email)

Each message is saved as a row in a Google Sheet, in a separate tab for every day
(e.g. `2026-09-27`). Nothing is emailed. It's free and takes about 5 minutes.

1. Open https://sheets.new and name the sheet, e.g. "Website messages".
2. Menu **Extensions → Apps Script**. Delete what's there and paste this:

```js
function doPost(e) {
  var p = (e && e.parameter) || {};
  if (p.website) return ContentService.createTextOutput('ok'); // spam trap
  var ss = SpreadsheetApp.getActiveSpreadsheet();
  var tz = Session.getScriptTimeZone();
  var now = new Date();
  var day = Utilities.formatDate(now, tz, 'yyyy-MM-dd');
  var sh = ss.getSheetByName(day);
  if (!sh) {
    sh = ss.insertSheet(day, 0);
    sh.appendRow(['Time', 'Name', 'Email', 'Message']);
    sh.setFrozenRows(1);
  }
  // Cap lengths and neutralise spreadsheet formulas (=, +, -, @)
  var clean = function (v, n) { v = String(v || '').slice(0, n); return /^[=+\-@\t\r]/.test(v) ? "'" + v : v; };
  sh.appendRow([Utilities.formatDate(now, tz, 'HH:mm:ss'), clean(p.name, 200), clean(p.email, 200), clean(p.message, 5000)]);
  return ContentService.createTextOutput('ok');
}
```

3. Click **Deploy → New deployment → ⚙ → Web app**.
   - Execute as: **Me**
   - Who has access: **Anyone**
   Click Deploy, allow the permissions, and copy the **Web app URL** (ends in `/exec`).
If you already deployed the old script: paste this version, then Deploy → Manage deployments → Edit → Version: New version.

4. Open `content/contact/content.md` and paste it after `formEndpoint:`

To read messages, open the sheet: the newest day is the first tab.
