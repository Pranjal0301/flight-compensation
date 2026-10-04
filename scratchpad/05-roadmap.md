# 05 — Roadmap

Solo pace, ~10–15 hrs/week. Dates from 2026-09-26. Scheduled as portfolio project #2, starting November.

## Phase 0 — Verify the two unknowns (2 hours, before any code)

- [ ] **Confirm the current EU261 and UK261 bands and thresholds.** Reform has been under discussion for years. The whole site is wrong if these moved.
- [ ] **Confirm claim-company affiliate terms.** Per submitted claim or per successful payout? Cookie window? Do they accept affiliate traffic at all?

**Gate:** if no claim company runs a usable affiliate programme, this becomes an ad-supported site and drops several places in the portfolio. Two hours decides it.

## Phase 1 — MVP (1 week)

- [ ] Buy domain, scaffold off the x-revenue template, deploy
- [ ] `lib/eligibility.ts` — pure, tested, versioned; the haversine distance and band logic
- [ ] Bundle `airports.json` and `airlines.json`
- [ ] Checker UI, mobile-first (this audience is standing in an airport)
- [ ] Free claim-letter generator
- [ ] Methodology page with dated rules, `llms.txt`, JSON-LD, sitemap
- [ ] 30 seeded route pages + 10 airline pages
- **Goal:** live, in Search Console, launched on r/travel and r/flying

## Phase 2 — Long tail (months 1–3)

- [ ] Expand to ~300 route pages; watch GSC coverage weekly before scaling further
- [ ] The objection guides — weather, strikes, technical faults, missed connections. **These are the highest-traffic pages on the site.**
- [ ] Per-airline claim guides for the 30 biggest carriers
- [ ] Referral placement at the post-result moment, alongside the free letter
- **Goals:** 200+ pages indexed · 5k visits/mo · first referral conversion

## Phase 3 — Seasonal capture (months 3–6)

- [ ] **Have disruption content ready before the season, not during.** Summer ATC strikes and winter weather are the traffic spikes this niche lives on.
- [ ] Historical on-time data per route as a separate content magnet
- [ ] Boarding-pass OCR autofill (client-side)
- [ ] Consider display ads past 10k sessions
- **Goals:** 20k visits/mo · $400+/mo

## Phase 4 — Expand

- US DOT regime (different rules — no cash mandate for delays, but real rights on cancellations and involuntary bumping)
- Canada APPR, Brazil ANAC
- Paid API for travel apps and insurers

## Kill / pivot criteria

- **Regulation changed materially and unfavourably** (threshold raised well above 3h) → the addressable market shrinks; reassess before building
- **No affiliate programme available** → ad-only, deprioritise
- **Under 3k visits/mo by month 4** despite 200 indexed pages → incumbents are dominating even the long tail; pivot to the free-letter tool as a link asset and move on

## Standing rule

**Date every regulatory claim on the site.** Same rule as HowMuchOnX. When the rules change, that dateline is what keeps the site honest instead of quietly wrong.
