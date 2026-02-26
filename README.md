
# Luxia Travel – Astro + GitHub Pages Starter

**Created:** 2026-02-25 04:10 UTC

This repository contains an Astro static site configured to deploy **free** on **GitHub Pages** via **GitHub Actions**.

## Quick Start

1. **Create a new public GitHub repository** and upload these files.
2. Go to **Settings → Pages → Build and deployment → Source = GitHub Actions**.
3. Push to `main`. The workflow in `.github/workflows/deploy.yml` will build and publish automatically.
4. Your site will appear at the URL shown in the Actions run (and under **Settings → Pages**).

> Docs: GitHub Pages supports publishing from a branch **or** via Actions. We use Actions here for a cleaner repo and automatic builds.

## Local Development

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
npm run preview
```

## Custom Domain (luxiatravel.com)

1. After your first successful publish, go to **Settings → Pages → Custom domain** and enter `luxiatravel.com`.
2. In your DNS provider, set:
   - **A records** for the apex (`luxiatravel.com`) pointing to GitHub Pages IPs (or use ALIAS/ANAME if supported).
   - **CNAME** for `www` → the GitHub Pages host for your site.
3. Once DNS propagates, enable **Enforce HTTPS** in **Settings → Pages**.

## Content
- Edit copy in `src/pages/*.astro` and add destinations under `content/destinations/`.
- Assets go in `public/`.

## Brand
- Colors: Sand `#E8DCC8`, Charcoal `#2A2A2A`, Warm White `#F8F5F1`, Gold Haze `#C9A878`.
- Typography: Inter by default (swap to Avenir/Neue Montreal when licensing allows).

## Notes
- This starter intentionally avoids committing a `/docs` build; GitHub Actions does the build & deploy.
- If you prefer the branch-based `/docs` method, change `Settings → Pages → Source = Deploy from a branch` and configure Astro `outDir: './docs'`.
