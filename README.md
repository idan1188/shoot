# Career Tools IL

Browser tools for salary talks and freelance quotes, for Israel. English is the default; Hebrew is available from the EN | HE toggle (saved in `localStorage` as `ctil_lang`). The osek explainer is the exception: with no saved choice it renders in Hebrew and does not write `ctil_lang` until a language is already saved or the toggle is used. The salary page is a Negotiation Command Center: ask, target, and walk-away, plus simulated employer counters, a three-message pack, an offer battle board, and a local session vault that exports one HTML brief pack. The freelance page is a Pricing OS: the same break-even and utilization math, a scope-to-price wizard, and bilingual replies when a client pushes the rate down. Patur stays ×1.28. Murshe stays ×1.35, with 17% VAT only on the invoice illustration. Illustrative estimates, not tax or career advice. Scroll progress, the hero rules, and section reveals use CSS scroll timelines where the browser supports them, with a small script otherwise. `prefers-reduced-motion: reduce` keeps the pages static.

Launch prices, with the original struck through on the page: bundle ₪43 (was ₪129), salary tool ₪26 (was ₪79), freelance tool ₪23 (was ₪69). Bought separately at the launch price that is ₪49 (was ₪148). The badge reads LAUNCH / השקה.

**Live:** https://idan1188.github.io/shoot/

Screenshots: social cards (Open Graph, Twitter, WhatsApp, LinkedIn) use [`preview.png`](preview.png) in the repo root. When the UI changes, replace that file and keep the filename `preview.png` so `og:image`, `twitter:image`, and `site.webmanifest` stay valid. It is a 1280×1600 PNG.

## Pages

| Path | Role |
| --- | --- |
| `index.html` | Landing, why-us sections, FAQ, share links, and local email capture (`#lead`) |
| `why/` | The full case: why us, problem and outcome, comparison with a free calculator, FAQ |
| `why-us/` | Why choose us: three numbers, language for the room, Israel, browser privacy, the employee and freelancer bundle. Launch prices ₪26 / ₪23 / ₪43. |
| `command-center/` | War room: employer-reply simulator, round log (`ctil_cc_rounds_v1`), six-message pack, two-offer compare, offline export. Reads `ctil_salary_v1`. Pro blocks link to `#lead` only. |
| `osek-patur-vs-murshah/` | Hebrew-first explainer of how the freelance calculator treats osek patur vs murshe. Not tax or legal advice. |
| `salary-negotiator/` | Salary brief. Existing command-center accessories stay. Header links to `/command-center/`. |
| `first-job-offer-israel/` | Preparation guide before accepting or negotiating a first job offer in Israel: ready-versus-guessing checklist, figures the visitor types, and email, WhatsApp, and call templates they rewrite. Not advice. |
| `promotion-interview-israel/` | Preparation guide for a promotion interview in Israel, in a role you already hold: a checklist of your own notes, current title, target title, and evidence you write, optional ask and floor, and email, WhatsApp, and talking-point drafts. Not advice. |
| `resign-counter-offer-israel/` | Preparation guide for a counter-offer after you already resigned or gave notice in Israel: a checklist of your own notes, the notice status and counter package you write, optional ask and floor, and email, WhatsApp, and talking-point drafts. Not the still-employed retention page. Not advice. |
| `freelance-rate/` | Pricing OS: scope wizard, objection replies, break-even and utilization on one desk. |
| `404.html` | Not-found page (EN default, HE toggle); nested misses still link back under `/shoot/` |

## Changelog

- War room at `/command-center/`: counter, stall, ask-first, final, and silence paths; local round log (max 8); six messages that rewrite with the zone and the round; copy, `.txt`, and print export; two-offer total-comp compare. Counter at a number reuses the salary sensitivity.
- Home, Why, and Why Us: launch wording. Hero is “Know the number before you say it.” Prices stay ₪26 / ₪23 / ₪43, framed as a launch. No checkout URLs.
| `robots.txt`, `sitemap.xml`, `site.webmanifest` | Crawl and install metadata |

Public CTAs stay on `#lead`. Tool Pro buttons stay “Pro soon” until a real checkout URL exists. Do not add payment keys, a `CNAME`, or placeholder tokens like `{{…}}`.

In-site links are relative (`./salary-negotiator/`, `../#lead`). There are no `localhost` URLs. Canonical, hreflang, and sitemap URLs use `https://idan1188.github.io/shoot/`.

Pushes to `main` publish via [`.github/workflows/pages.yml`](.github/workflows/pages.yml). Deploy notes: [README_DEPLOY.md](README_DEPLOY.md).
