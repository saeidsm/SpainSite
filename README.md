# AlumGlass Spain Site (Cloudflare Pages)

Static multilingual site for **ALUMGLASS SPAIN, S.L.** with launch-ready pages in:

- English (`/en`)
- Spanish (`/es`)
- German (`/de`)

## Structure

- `index.html` (redirect to `/en/index.html`)
- `en/*.html`
- `es/*.html`
- `de/*.html`
- `assets/styles.css`
- `.github/workflows/deploy-cloudflare-pages.yml`

## Deploy on GitHub Actions

This repository is configured for automatic deploy to Cloudflare Pages on push to `main`.

Add these GitHub repository secrets:

- `CLOUDFLARE_API_TOKEN`
- `CLOUDFLARE_ACCOUNT_ID`
- `CLOUDFLARE_PAGES_PROJECT` (e.g. `alumglass-es`)

Workflow command:

```bash
pages deploy . --project-name=$CLOUDFLARE_PAGES_PROJECT
```

## Engineering tools

- `/fireproofing/index.html` — Persian (RTL, Vazirmatn) dashboard for structural
  engineers: input the column **section factor (Hp/A)**, pick a fire resistance
  rating (60/90/120 min), and the steel skeleton tonnage. It returns a suggested
  fire-protection coating thickness and the required material mass for **Proterm
  (350 kg/m³)** versus a user-defined competitor brand density, with a visual
  comparison. Self-contained single file (no build step).

## Content notes

- Company legal details are published under `/en/legal.html`, `/es/legal.html`, `/de/legal.html`.
- Contact email: `info@alumglass.es`
