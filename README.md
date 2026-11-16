# TRAKIO — Crypto P&L Tracker (v4.2.0)

## Files
- `index.html` — main app page (required; keep at the site root).
- `manifest.json` — installable PWA metadata.
- `service-worker.js` — offline cache and local notifications.
- `assets/icons/` — app icons.

## Deploy to GitHub Pages
1. Extract this ZIP.
2. Open the extracted folder. You should see `index.html` directly beside `manifest.json`.
3. Upload **all files and folders inside the ZIP** to the repository root (not an extra nested folder).
4. Enable GitHub Pages from the repository's main branch and root folder.
5. Open the HTTPS Pages URL in Chrome/Safari.

Do not open `index.html` directly with `file://` for normal use. TRAKIO uses Web Crypto and service workers; HTTPS (GitHub Pages) or `http://localhost` is required for full functionality.

## Clean account reset (v4.2.0)
- On the first launch of v4.2.0, TRAKIO removes previous local account records, encrypted ledger data, old recovery material and login lockout state from this browser. This is intentional and irreversible unless you previously exported a backup.
- After this one-time reset, create a new account.

## Login / account setup
- First launch: create an account with a name, contact and password of at least 8 characters.
- Later launches: enter the password to unlock.
- Forgot password: enter the same registered contact, verify the local notification/in-app OTP, then set a new password. No Recovery Key is requested. The same browser profile must retain its device recovery material.
- OTP is generated on this device; it is **not SMS** and does not verify phone ownership.

## Data & recovery warning
Trades are encrypted locally in this browser. Password recovery uses a device-local key stored in this browser profile. Recovery is therefore limited to the same browser/device profile. Clearing site data or switching devices/profiles can remove the recovery material. Export regular backups from inside the app.

## Ledger PDF and transaction invoices
- Open **Ledger** and choose the period from the **Show** selector.
- Tap **Download Ledger PDF**. Your browser's print screen opens; choose **Save as PDF**. The report follows the selected period.
- Tap **Invoice** beside an individual trade or expense to print/save a trade receipt or expense voucher as PDF.
- These are personal record-keeping documents generated from your own entries, not exchange-issued or tax invoices.
