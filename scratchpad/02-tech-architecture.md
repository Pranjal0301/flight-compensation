# 02 — Tech Architecture

## Stack

| Layer | Choice | Why |
|---|---|---|
| Framework | **Next.js 16 (App Router)** | Reuse the x-revenue template wholesale |
| Hosting | **Vercel** | Fully static build — this site has no runtime data needs at all |
| Database | **None** | Nothing to store. Optionally a Supabase table for claim-letter analytics later. |
| Data | **Bundled JSON** | Airport coordinates ship with the repo |

**This is the cheapest site in the portfolio to run and the least likely to break.** No external API is on the critical path.

## The eligibility engine (`lib/eligibility.ts`)

Same discipline as `x-revenue/lib/estimator.ts`: **pure functions, no I/O, unit tested, versioned.** Never compute a compensation figure anywhere else.

```
compensation = band(great_circle_km(origin, destination))
             x eligible(delay_hours, cause, jurisdiction)

band:  <= 1500 km              -> EUR 250
       1500-3500 km            -> EUR 400
       > 3500 km               -> EUR 600
       (UK261 mirrors in GBP)

eligible: delay >= 3h
          AND departs EU/UK, or arrives EU/UK on an EU/UK carrier
          AND cause is not an extraordinary circumstance
          AND within the claim window for that jurisdiction
```

`RULES_VERSION` lives in this file and renders on the methodology page. **If the regulation changes, bump it** — exactly the rule x-revenue applies to its rate bands.

Reduced-compensation edge case: re-routing within certain time windows can halve the award. Model it, test it, do not hand-wave it.

## Data

```
data/airports.json     IATA code, name, city, country, lat, lon  (~5,000 rows)
data/airlines.json     IATA code, name, country, EU/UK carrier flag
data/jurisdictions.json claim window in years, currency, authority to complain to
```

All static, all public, all bundled. Great-circle distance is the haversine formula — a pure function with tests.

## Repo layout

```
/app
  /page.tsx                        the checker
  /route/[origin]-[destination]/   programmatic route pages
  /airline/[iata]/                 per-airline guides
  /guides/[slug]/                  regulation explainers
  /methodology/                    the rules, dated — the AEO target
  /api/check/route.ts              JSON endpoint
/lib/eligibility.ts                pure logic + tests
/lib/letter.ts                     claim-letter generator, also pure
/data/                             bundled static JSON
/content/guides/                   one .md per guide
```

## Why this stays cheap forever

Airport coordinates do not move. Distance bands are in a regulation. There is no refresh cron, no API key, no rate limit, no vendor. The only maintenance is watching for regulatory change — and that is a news event, not an outage.
