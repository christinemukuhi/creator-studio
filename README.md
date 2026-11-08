# Creator Studio

A personal planner for a digital products shop: products and launches, files with automatic version archiving,
an ideas board, a pricing calculator with platform fees, sales and revenue tracking, a Pinterest plan with a
month calendar, and backups. It runs entirely in your browser and installs like an app.

## What is in this folder

| File | What it does |
|---|---|
| `index.html` | The whole app. This is the file you edit or replace to update the app. |
| `manifest.webmanifest` | Tells browsers the app can be installed (name, colours, icons). |
| `sw.js` | Lets the app open offline and fetch the newest version whenever you are online. |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | App icons. |
| `.nojekyll` | Tells GitHub to serve the files as they are. Optional; it is a hidden file. |

## Put it on GitHub Pages (no command line needed)

1. Sign in at github.com and click **New repository**. Name it, for example, `creator-studio`.
   A free account needs the repository to be **Public** for GitHub Pages. (Your *data* is never in the repo; see below.)
2. On the new repository page click **uploading an existing file**, drag in every file from this folder, and click **Commit changes**.
3. Open **Settings > Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*,
   choose branch **main** and folder **/ (root)**, then **Save**.
4. Wait a minute or two. Your app will be at `https://YOUR-USERNAME.github.io/creator-studio/`.
   GitHub shows the exact link at the top of the Pages settings.

If you prefer the command line: `git init`, `git add .`, `git commit -m "first version"`, add your GitHub remote, `git push -u origin main`, then do step 3.

## Install it like an app

- **Chrome or Edge (laptop):** click the install icon at the right end of the address bar, or **Settings > Install app** inside the app.
- **Android (Chrome):** menu, then **Install app**.
- **iPhone or iPad (Safari):** tap **Share**, then **Add to Home Screen**.

## Updating the app later

1. Get the new `index.html` (or other changed files).
2. In your repository click the file, then the pencil or **Upload files**, replace it, and **Commit changes**.
3. After about a minute the new version is live. Open or reload the app while online and you get it.
   The app uses a network-first service worker, so there is no stale copy to clear.
   If you ever see an old version, open **Settings > Check for updates**, then reload.

Your data is stored separately from the code, so updating the app never touches your products, sales or files.

## Your data: read this

- Everything (products, sales, ideas, pins, settings) is stored **in this browser, on this device only**.
  There is no account and no sync. Installing the app on your phone and your laptop gives you two separate copies.
- Uploaded files are stored in the browser too (IndexedDB). They are **not** included in the backup file.
  Keep your original files somewhere safe as well.
- Clearing site data, using a private window, or deleting the app can erase everything.
  Browsers may also clear storage for sites you rarely use.
  **Download a backup from the Dashboard regularly** (Backup > Download backup).
- To move to another device or browser: download a backup, open the app there, click **Restore from backup**,
  then re-upload your files.

## Moving over from the Claude-hosted version

1. In the old version go to the Dashboard and click **Download backup**.
2. Open the new app, go to the Dashboard and click **Restore from backup**.
3. Your products, sales, ideas, pins and settings come across. Files do not: the old file list appears, but opening
   one says it is not stored in this browser. Download your originals from the old version first, then upload them again.
4. The two versions do not sync. Use one of them from then on.

## Privacy

The code is public if the repository is public, but nobody can see your data. It never leaves your browser.
Google Fonts are loaded from Google if you are online; offline the app falls back to system fonts.
