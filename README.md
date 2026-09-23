# Career Tools IL

Browser tools for salary talks and freelance quotes, for Israel. English is the default; Hebrew is available from the EN | HE toggle (saved in `localStorage` as `ctil_lang`). The osek explainer is the exception: with no saved choice it renders in Hebrew, and it writes `ctil_lang` only after the toggle is used. The salary brief gives an ask, a target, a walk-away, a counter ladder, and a leverage score. The freelance quote gives a break-even rate, a commercial rate with margin, utilization sensitivity, and an editable proposal. Illustrative estimates, not tax or career advice. Scroll progress, the hero rules, and section reveals use CSS scroll timelines where the browser supports them, with a small script otherwise. `prefers-reduced-motion: reduce` keeps the pages static.

Sale prices, with the original struck through on the page: bundle ₪43 (was ₪129), salary tool ₪26 (was ₪79), freelance tool ₪23 (was ₪69). Bought separately on sale that is ₪49 (was ₪148).

**Live:** https://idan1188.github.io/shoot/

Screenshots: social cards (Open Graph, Twitter, WhatsApp, LinkedIn) use [`preview.png`](preview.png) in the repo root. When the UI changes, replace that file and keep the filename `preview.png` so `og:image`, `twitter:image`, and `site.webmanifest` stay valid. It is a 1280×1600 PNG.

## Pages

| Path | Role |
| --- | --- |
| `index.html` | Landing, FAQ, share links, and local email capture (`#lead`) |
| `why-us/` | Why these calculators: live formulas, Israel heuristics, offline files |
| `osek-patur-vs-murshah/` | Educational osek patur vs murshe pricing explainer (not tax advice) |
| `salary-negotiator/` | Salary brief: ask, target, walk-away, counter ladder |
| `freelance-rate/` | Freelance quote: margin, sensitivity, editable proposal |
| `404.html` | Not-found page (EN default, HE toggle); nested misses still link back under `/shoot/` |
| `robots.txt`, `sitemap.xml`, `site.webmanifest` | Crawl and install metadata |

Public CTAs stay on `#lead`. Tool Pro buttons stay “Pro soon” until a real checkout URL exists. Do not add payment keys, a `CNAME`, or placeholder tokens like `{{…}}`.

In-site links are relative (`./salary-negotiator/`, `../#lead`). There are no `localhost` URLs. Canonical, hreflang, and sitemap URLs use `https://idan1188.github.io/shoot/`.

Pushes to `main` publish via [`.github/workflows/pages.yml`](.github/workflows/pages.yml). Deploy notes: [README_DEPLOY.md](README_DEPLOY.md).
