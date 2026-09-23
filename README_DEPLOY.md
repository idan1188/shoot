# Career Tools IL — Deploy (GitHub Pages / Netlify)

Static Hebrew micro-site wrapping both interactive tools.

**Intended live URL:** https://idan1188.github.io/shoot/

```
career-tools-il/
  index.html              # landing + FAQ + local lead capture
  salary-negotiator/      # salary negotiator tool
  freelance-rate/         # freelance rate tool
  preview.png             # Open Graph / social preview
  robots.txt
  sitemap.xml
  404.html
  site.webmanifest
  .nojekyll               # required for GitHub Pages (skip Jekyll)
  netlify.toml            # optional Netlify redirects/headers
  _headers
  README_DEPLOY.md
```

## Public UX (no payment accounts required)

- Landing CTAs point to `#lead` — visitors leave an email locally; success copy: «נתקשר אליכם עם קישור הרכישה».
- Price **₪129** stays visible on the bundle card.
- Tool Pro buttons are disabled gracefully: «Pro בקרוב · השאירו מייל בדף הבית» (no live checkout URLs).
- No Formspree / Payhip / affiliate placeholders are shown to visitors.

When you later have real checkout URLs, swap `#lead` / tool Pro hrefs in the HTML — do not reintroduce literal `{{…}}` tokens on the live site.

---

## Option A — GitHub Pages (primary)

Repo expected: `idan1188/shoot` → site at `https://idan1188.github.io/shoot/`

1. Put **this folder’s contents** at the repo root (not nested inside another `career-tools-il/` folder).
2. Push to `main` (or `gh-pages`).
3. Repo → **Settings → Pages** → Source: Deploy from a branch → `main` / `/ (root)`.
4. Confirm `.nojekyll` is present so Pages does not run Jekyll.
5. **Do not** add a `CNAME` until you have a custom domain.

### Base path `/shoot/` — critical

All nav/asset links in this site are **relative** (`./salary-negotiator/`, `../#lead`, `./preview.png`).  
They work under `https://idan1188.github.io/shoot/` and also on Netlify root deploys.

Avoid absolute-root paths like `/salary-negotiator/` — those would resolve to `github.io/salary-negotiator/` and break on project Pages.

Canonical / Open Graph / sitemap URLs use the absolute base  
`https://idan1188.github.io/shoot/`.

### Netlify short redirects vs Pages

`netlify.toml` maps `/salary` → `/salary-negotiator/` (and similar).  
**GitHub Pages does not read `netlify.toml`.** Use the full paths, or add equivalent Pages redirects later (Action / `404.html` tricks). Documented here so you do not expect `/salary` to work on Pages out of the box.

---

## Option B — Netlify (drag-drop)

1. https://app.netlify.com/ → Add new site → Deploy manually
2. Drag this folder onto the drop zone
3. Optional: link Git; base directory = this folder; build empty; publish `.`

## Smoke test after deploy

1. Open `/shoot/` (or Netlify root) — hero + two tool cards
2. Open `/shoot/salary-negotiator/` and `/shoot/freelance-rate/` — calculators work
3. Bundle / nav CTAs scroll to `#lead`; submit email → localStorage success message (no network form)
4. Pro buttons show «בקרוב» and do not navigate to a payment placeholder
5. `robots.txt`, `sitemap.xml`, `404.html` reachable; OG image loads from `/shoot/preview.png`

## Do not

- Commit payment API keys / secrets into this folder
- Publish with literal payment/form placeholder tokens visible in the UI
- Add `CNAME` before a custom domain is ready
