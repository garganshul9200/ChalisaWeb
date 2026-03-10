# Chalisa Sangrah – Web Landing Page

This repository contains the simple, static landing page for the **Chalisa Sangrah** Android app – a calm space to read about the app, find the Play Store link, and view basic contact / policy information.

The site is intentionally lightweight HTML + CSS, with no build tooling required.

## Structure

- **`public/index.html`** – main marketing page with hero section, app description, and contact details.
- **`public/privacy.html`** – privacy policy for the app.
- **`public/terms.html`** – terms &amp; conditions for the app.
- **`public/app-ads.txt`** – ads configuration for the Play Store.

You can serve the `public` directory with any static file host (Firebase Hosting, Netlify, Vercel, GitHub Pages, etc.).

## Local development

No build step is required. You can open `public/index.html` directly in a browser, or run a tiny static server:

```bash
cd public
python3 -m http.server 8000
```

Then visit `http://localhost:8000` in your browser.

## Deployment

- Upload the contents of `public/` to your static hosting provider, or
- Point your hosting configuration to use `public` as the document root.

Make sure that:

- `index.html` is set as the default document.
- `privacy.html`, `terms.html`, and `app-ads.txt` are accessible at the root (e.g. `/privacy.html`).

## Updating Play Store links

The primary Play Store link appears:

- In the hero button (`Get the Android app`).
- In the footer “Available on Google Play” badge.

If the Play Store URL changes, search for `play.google.com/store/apps/details?id=` in `index.html` and update both occurrences.