# Fairway Fuel — Installable iPhone PWA

A self-contained, privacy-friendly nutrition and workout tracker built with HTML, CSS and JavaScript. No build tools, Apple computer, or subscription required.

## What's included
- Dashboard with daily meal calories and protein totals, date selector, and workout sessions
- Preloaded food history for November 3–4, 2026, including Panda Express
- Preloaded November 3 workouts (back/biceps, abs, basketball)
- Add and delete meals, workouts, and optional weight measurements
- 14-day progress chart for calories, protein and training sessions
- Local data persistence, JSON export/import, and service-worker offline caching
- Standalone iPhone Home Screen icon and web app manifest

## Publish for free using a Windows laptop — GitHub Pages

1. Extract `FairwayFuel-PWA.zip` to a folder. The extracted folder contains `index.html`, `app.js`, `styles.css`, `sw.js`, `manifest.webmanifest`, and `icons/`.
2. Sign in to [github.com](https://github.com) and create a **public** repository named `fairway-fuel` (or another name). GitHub Pages on a free account supports public repositories. Note that **source code** will be public, but your personal food logs entered later are stored locally and are not uploaded. The starter November 3–4 logs are part of the public source files; remove them before publishing if you don't want them public.
3. Choose **Add file → Upload files**, and upload **the contents** of the extracted folder, including the `icons` directory, into the repository root. Commit the files.
4. Open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**; choose branch **main** and folder **/(root)**, then save.
5. Wait for deployment, then open `https://YOUR-USERNAME.github.io/fairway-fuel/` (replace `YOUR-USERNAME` and repo name). The actual URL is also shown in GitHub's Pages settings.
6. On your iPhone, open that HTTPS address in **Safari**. Tap **Share → Add to Home Screen → Add** (the exact wording may vary by iOS version).
7. Launch Fairway Fuel from the new Home Screen icon **while online once**. It will cache the app for offline use. Add a test meal, close and reopen it, and verify the entry persists.

## Alternative hosting
Netlify Drop also supports uploading the extracted site folder to create an HTTPS website. Hosting interfaces and free-tier policies may change.

## Local testing on Windows
You can open `index.html` directly to preview the interface, but offline caching/service workers require HTTPS or localhost. For a proper local test, open a terminal in the folder and run `python -m http.server 8000` if Python is installed, then visit `http://localhost:8000` in a browser.

## Data and privacy
- New entries are stored in browser `localStorage` on **each device separately**. There is no server or account, and no automatic sync with ChatGPT or between laptop and phone.
- To transfer data, use **Settings → Export backup** on one device, then **Settings → Import backup** on the other. Import **replaces** existing entries; it does not merge.
- Export backups regularly. Removing the Home Screen app or clearing website data may erase locally stored logs.
- The original November 3–4 food and workout logs are seeded in `app.js`. Anyone with access to the public repository can see these seed records. To keep those logs private, remove them from the seed before public hosting and import them later from a private JSON backup.
- Nutrition numbers are approximate and should not be used as strict limits or medical guidance.

## Files
- `index.html`: app interface
- `styles.css`: layout and styling
- `app.js`: app logic, starter logs and local data
- `manifest.webmanifest`: installation metadata
- `sw.js`: offline caching
- `icons/`: app icons
