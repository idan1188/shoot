# Career Tools IL

Browser tools for salary talks and freelance quotes, for Israel. English is the default; Hebrew is available from the EN | HE toggle (saved in `localStorage` as `ctil_lang`). The osek explainer is the exception: with no saved choice it renders in Hebrew and does not write `ctil_lang` until a language is already saved or the toggle is used. The salary brief gives an ask, a target, a walk-away, a counter ladder, and a leverage score. The freelance quote gives a break-even rate, a commercial rate with margin, utilization sensitivity, and an editable proposal. Illustrative estimates, not tax or career advice. Scroll progress, the hero rules, and section reveals use CSS scroll timelines where the browser supports them, with a small script otherwise. `prefers-reduced-motion: reduce` keeps the pages static.

Launch prices, with the original struck through on the page: bundle ₪43 (was ₪129), salary tool ₪26 (was ₪79), freelance tool ₪23 (was ₪69). Bought separately at the launch price that is ₪49 (was ₪148). The badge reads LAUNCH / השקה.

**Live:** https://idan1188.github.io/shoot/

Screenshots: social cards (Open Graph, Twitter, WhatsApp, LinkedIn) use [`preview.png`](preview.png) in the repo root. When the UI changes, replace that file and keep the filename `preview.png` so `og:image`, `twitter:image`, and `site.webmanifest` stay valid. It is a 1280×1600 PNG.

## Pages

| Path | Role |
| --- | --- |
| `index.html` | Landing, why-us sections, FAQ, share links, and local email capture (`#lead`) |
| `why/` | The full case: why us, problem and outcome, comparison with a free calculator, FAQ |
| `why-us/` | Why these calculators: live formulas, Israel heuristics, offline files. Sale prices ₪26 / ₪23 / ₪43. English default. |
| `osek-patur-vs-murshah/` | Hebrew-first explainer of how the freelance calculator treats osek patur vs murshe. Not tax or legal advice. |
| `salary-negotiator/` | Salary brief: presets, two offers, bonus, editable counter ladder |
| `freelance-rate/` | Freelance quote: presets, utilization stress, package builder, proposal clauses |
| `404.html` | Not-found page (EN default, HE toggle); nested misses still link back under `/shoot/` |
| `robots.txt`, `sitemap.xml`, `site.webmanifest` | Crawl and install metadata |

Public CTAs stay on `#lead`. Tool Pro buttons stay “Pro soon” until a real checkout URL exists. Do not add payment keys, a `CNAME`, or placeholder tokens like `{{…}}`.

In-site links are relative (`./salary-negotiator/`, `../#lead`). There are no `localhost` URLs. Canonical, hreflang, and sitemap URLs use `https://idan1188.github.io/shoot/`.

Pushes to `main` publish via [`.github/workflows/pages.yml`](.github/workflows/pages.yml). Deploy notes: [README_DEPLOY.md](README_DEPLOY.md).
