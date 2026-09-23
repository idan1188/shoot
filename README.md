# Career Tools IL

Browser calculators for salary negotiation and freelance rates, for Israel. English is the default; Hebrew is available from the EN | HE toggle (saved in `localStorage` as `ctil_lang`). Try them in the browser — counter-range, walk-away number, hourly/daily rate, and a quote you can copy. Illustrative estimates, not tax or career advice.

Sale prices, with the original struck through on the page: bundle ₪43 (was ₪129), salary tool ₪26 (was ₪79), freelance tool ₪23 (was ₪69). Bought separately on sale that is ₪49 (was ₪148).

**Live:** https://idan1188.github.io/shoot/

Screenshots: social cards (Open Graph, Twitter, WhatsApp, LinkedIn) use [`preview.png`](preview.png) in the repo root. When the UI changes, replace that file and keep the filename `preview.png` so `og:image`, `twitter:image`, and `site.webmanifest` stay valid. It is a 1280×1600 PNG.

## Pages

| Path | Role |
| --- | --- |
| `index.html` | Landing, FAQ, share links, and local email capture (`#lead`) |
| `salary-negotiator/` | Salary negotiator |
| `freelance-rate/` | Freelance rate calculator |
| `404.html` | Not-found page (EN default, HE toggle); nested misses still link back under `/shoot/` |
| `robots.txt`, `sitemap.xml`, `site.webmanifest` | Crawl and install metadata |

Public CTAs stay on `#lead`. Tool Pro buttons stay “Pro soon” until a real checkout URL exists. Do not add payment keys, a `CNAME`, or placeholder tokens like `{{…}}`.

In-site links are relative (`./salary-negotiator/`, `../#lead`). There are no `localhost` URLs. Canonical, hreflang, and sitemap URLs use `https://idan1188.github.io/shoot/`.

Pushes to `main` publish via [`.github/workflows/pages.yml`](.github/workflows/pages.yml). Deploy notes: [README_DEPLOY.md](README_DEPLOY.md).
