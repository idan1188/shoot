# Career Tools IL

Interactive Hebrew career tools (salary negotiator and freelance rate calculator). Static site for GitHub Pages.

**Live URL:** https://idan1188.github.io/shoot/

## What’s in this repo

| Path | Role |
| --- | --- |
| `index.html` | Landing, FAQ, and local email capture (`#lead`) |
| `salary-negotiator/` | Salary negotiator tool |
| `freelance-rate/` | Freelance rate tool |
| `preview.png` | Open Graph / social preview |
| `robots.txt`, `sitemap.xml`, `404.html`, `site.webmanifest` | SEO and PWA metadata |
| `.nojekyll` | Tells GitHub Pages to skip Jekyll |
| `.github/workflows/pages.yml` | Deploy static files with GitHub Actions |
| `netlify.toml`, `_headers` | Optional Netlify headers/redirects (Pages ignores these) |

Public CTAs point at `#lead`. Tool Pro buttons stay disabled («Pro בקרוב») until real checkout URLs exist. Do not add payment keys, a `CNAME`, or placeholder tokens like `{{…}}`.

## Deploy

Pushes to `main` run [`.github/workflows/pages.yml`](.github/workflows/pages.yml) (no build step). Pages source must be **GitHub Actions**.

The cloud token used to push this repo cannot turn Pages on (`administration: write` is required). One-time setup, as the repo owner:

1. Open [Settings → Pages](https://github.com/idan1188/shoot/settings/pages).
2. Under **Build and deployment**, set **Source** to **GitHub Actions** and save.
3. Re-run [Deploy GitHub Pages](https://github.com/idan1188/shoot/actions/workflows/pages.yml).

After that, every push to `main` publishes the site.

Canonical and sitemap URLs use `https://idan1188.github.io/shoot/`. In-site links are relative (`./salary-negotiator/`, `../#lead`) so they work on this project site. Short paths such as `/salary` exist only in `netlify.toml` and do not redirect on GitHub Pages.

More detail: [README_DEPLOY.md](README_DEPLOY.md).
