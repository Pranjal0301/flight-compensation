# Flight Delay Compensation Checker — Scratchpad

Tells a passenger whether their delayed or cancelled flight owes them money under EU261 / UK261, and how much.

**Started:** 2026-09-26 · **Portfolio rank:** #2 of 6 (best effort-to-return ratio)

## Docs

1. [01-product-plan.md](01-product-plan.md) — problem, solution, MVP scope, competitors
2. [02-tech-architecture.md](02-tech-architecture.md) — stack and the eligibility engine
3. [03-seo-strategy.md](03-seo-strategy.md) — programmatic route pages, keyword targets, AEO
4. [04-domains.md](04-domains.md) — domain candidates + the airline trademark trap
5. [05-roadmap.md](05-roadmap.md) — phases, milestones, kill criteria
6. [06-revenue-projections.md](06-revenue-projections.md) — how the site makes money

## One-line pitch

> Your flight was three hours late. You are probably owed up to €600 and nobody told you. Enter the flight, find out in ten seconds.

## Why this is ranked #2

**The data never changes.** Airport coordinates, distance bands, and the regulation are static. There is no API to break, no scraping, no pipeline to maintain, no rate limits. Build it once and it runs for years.

Meanwhile a converted claim is worth $20–60 in referral fees — thousands of times a display-ad pageview.

## Raw idea dump

- Upload a boarding pass and auto-fill the form (OCR, client-side)
- "Was your flight actually delayed?" — historical on-time data per route as a separate content magnet
- Compensation letter generator — free, and a genuinely better lead than a referral click
- Airline-by-airline guides: who pays without a fight, who stonewalls
- Extraordinary-circumstances explainer — the #1 reason claims get refused, and the #1 thing airlines lie about
- Deadline calculator: the claim window varies by country, 2–6 years. People miss it.
- Expand to US DOT rules (different regime, no cash mandate for delays, but real rights on cancellations and bumping)
