# Quran Trackers

Two standalone PWA-ready trackers, each installable on Chrome via "Add to Home Screen":
- `manzil-tracker.html` — Manzil Tracker
- `murajaah-tracker.html` — Quran Murajaah Tracker (7-Station SRS)

`index.html` is a simple landing page linking to both.

## Deploy to GitHub Pages

1. Create a new repo (via web UI, or CLI below):
   ```bash
   cd quran-trackers
   git init
   git add .
   git commit -m "Initial deploy: Quran trackers"
   gh repo create quran-trackers --public --source=. --push
   ```
   (No `gh` CLI? Create the repo manually on github.com, then:
   ```bash
   git remote add origin https://github.com/<your-username>/quran-trackers.git
   git branch -M main
   git push -u origin main
   ```
   )

2. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main, folder: / (root) → Save**

3. Wait ~1 minute. Your site will be live at:
   `https://<your-username>.github.io/quran-trackers/`

## Install on your phone

1. Open the GitHub Pages URL in Chrome on your phone (either the index page, or go straight to `manzil-tracker.html` / `murajaah-tracker.html`)
2. Tap the ⋮ menu → **Add to Home screen** (or you may see **Install app**)
3. Confirm — it'll install as its own icon and open full-screen (no browser bar), thanks to the manifest.

## Updating later

Whenever you edit either HTML file:
```bash
git add .
git commit -m "update tracker"
git push
```
GitHub Pages auto-redeploys within a minute or two. No need to reinstall on your phone — it'll pick up changes next time it's opened (may need a manual refresh/reload once).
