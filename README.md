# Chalisa Sangrah – Web Landing Page

This repository contains the static landing page for the **Chalisa Sangrah** Android app ([AllChalisaApp](https://github.com/garganshul9200/AllChalisaApp)) — a calm space to read and listen to 32 popular Hindu Chalisas.

The site is intentionally lightweight HTML + CSS, with no build tooling required. It is deployed to Firebase Hosting (`allchalisaapp` project).

## Structure

- **`public/index.html`** – main marketing page with hero, features, full Chalisa list, and contact details.
- **`public/privacy.html`** – privacy policy for the app.
- **`public/terms.html`** – terms & conditions for the app.
- **`public/app-ads.txt`** – AdMob ads.txt for Google Play (`pub-2848005220802634`).

## App at a glance

| Detail | Value |
|--------|-------|
| App name | Chalisa Sangrah |
| Package ID | `com.allchalisaapp` |
| Chalisas | 32 (offline text) |
| Audio | 8 Chalisas with streaming playback |
| Contact | anshuwebnetwork@gmail.com |

## Local development

No build step is required. Open `public/index.html` directly in a browser, or run a static server:

```bash
cd public
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deployment

Deployed automatically to Firebase Hosting on merge to `main` via GitHub Actions.

Manual deploy:

```bash
firebase deploy --only hosting
```

Make sure that `index.html`, `privacy.html`, `terms.html`, and `app-ads.txt` are accessible at the site root.

## Updating Play Store links

The Play Store link appears in the hero button and footer badge. Search for `play.google.com/store/apps/details?id=com.allchalisaapp` in the HTML files to update.
