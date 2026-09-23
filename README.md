# Career Tools IL

מחשבונים בעברית למשא ומתן על שכר ולתעריף פרילנס. נסו בדפדפן, בלי התקנה — טווח נגד, מספר יציאה, תעריף שעתי/יומי והצעת מחיר להעתקה. הערכות אילוסטרטיביות, לא ייעוץ מס או קריירה.

**Live:** https://idan1188.github.io/shoot/

Screenshots: social cards (Open Graph, Twitter, WhatsApp, LinkedIn) use [`preview.png`](preview.png) in the repo root. When the UI changes, replace that file and keep the filename `preview.png` so `og:image`, `twitter:image`, and `site.webmanifest` stay valid. It is a 1280×1600 PNG.

## Pages

| Path | Role |
| --- | --- |
| `index.html` | Landing, FAQ, share links, and local email capture (`#lead`) |
| `salary-negotiator/` | Salary negotiator |
| `freelance-rate/` | Freelance rate calculator |
| `404.html` | Hebrew not-found page; nested misses still link back under `/shoot/` |
| `robots.txt`, `sitemap.xml`, `site.webmanifest` | Crawl and install metadata |

Public CTAs stay on `#lead`. Tool Pro buttons stay «Pro בקרוב» until a real checkout URL exists. Do not add payment keys, a `CNAME`, or placeholder tokens like `{{…}}`.

In-site links are relative (`./salary-negotiator/`, `../#lead`). There are no `localhost` URLs. Canonical, hreflang, and sitemap URLs use `https://idan1188.github.io/shoot/`.

Pushes to `main` publish via [`.github/workflows/pages.yml`](.github/workflows/pages.yml). Deploy notes: [README_DEPLOY.md](README_DEPLOY.md).
