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

## Content notes

- Company legal details are published under `/en/legal.html`, `/es/legal.html`, `/de/legal.html`.
- Contact email: `info@alumglass.es`
