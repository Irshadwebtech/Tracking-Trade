TRAKIO PWA FIX — APPLY TO YOUR EXISTING REPOSITORY

Your existing icon files are in the repository root, but the current HTML,
manifest and service worker point to assets/icons/. This fix keeps your
existing folder layout and updates the references.

1) Replace manifest.json in the repository root with the manifest.json in this ZIP.
2) Replace service-worker.js in the repository root with the service-worker.js in this ZIP.
3) Edit your EXISTING index.html (do not replace the whole file):
   Replace:
     assets/icons/apple-touch-icon.png
   With:
     ./apple-touch-icon.png

   Replace:
     assets/icons/icon-192.png
   With:
     ./icon-192.png

   These are the two icon path references in the <head> of the current index.html.
   Leave the inline application script, its Content-Security-Policy hash, login,
   encryption, local storage and ledger code unchanged.
4) Commit the three changed files to the main branch.
5) Wait for GitHub Pages to publish, then open:
   https://irshadwebtech.github.io/Tracking-Trade/

6) In Chrome on Android, open the site, tap the three-dot menu and choose
   Install app (or Add to Home screen if that is the offered wording).

IMPORTANT:
- Do not delete your existing icon PNG files.
- Do not clear browser storage or app data; that could erase locally stored trades/accounts.
- This fixes the confirmed incorrect icon/cache paths. It does not guarantee installation
  until the deployed site is tested in Chrome.
- If an older service worker is already installed, close the app, revisit the website
  online, refresh once, then try installation again.
