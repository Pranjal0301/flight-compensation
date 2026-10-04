# 01 — Product Plan

## Problem

Under EU261 (and the UK's near-identical retained version), a passenger delayed 3+ hours on a qualifying flight is owed a fixed cash sum — up to €600 — regardless of ticket price. The right has existed for two decades.

Most passengers never claim. Two reasons:

1. **They do not know the right exists.** Airlines are not required to advertise it and do not.
2. **When they do, the first search result is a claim company** that takes 25–35% and gives no free answer first.

There is no good, free, neutral "am I eligible, and for how much" tool that just *answers the question*.

## Solution

```
Flight:   LHR → JFK, 3 Aug 2026, delayed 4h20m
  ├── Distance band   5,555 km → over 3,500 km
  ├── Delay           4h20m → qualifies (3h+ threshold)
  ├── Jurisdiction    Departed UK → UK261 applies
  └── You are likely owed  £520
       Claim it free yourself (template letter) or hand it to a service
```

Two honest exits, both fine for the business:

- **Free letter generator** — costs nothing, builds enormous trust and links
- **Hand it to a claim service** — for people who would rather lose 30% than chase an airline. This is the referral revenue.

## MVP scope (ship in ~1 week)

- Eligibility checker: airports, date, delay length, cause
- Distance calculation and compensation band
- Jurisdiction logic (departing EU/UK, or arriving on an EU/UK carrier)
- Plain-English result including *why* — and the extraordinary-circumstances caveat
- Free claim-letter generator
- ~30 seeded route and airline pages

## NOT in MVP

- Live flight status lookup (paid APIs; not needed — the passenger already knows their delay)
- Actually handling claims (that is a regulated business, not a website)
- Accounts, saved claims
- US DOT regime (v2)

## Competitors

| Who | What | Gap we exploit |
|---|---|---|
| AirHelp, Flightright, ClaimCompass | Claim companies, take 25–35% | They want your claim, not your question. No free neutral answer. |
| Which? / consumer sites | Good explainers | Static articles, no per-flight calculator |
| Airline help pages | Legally minimal | Actively unhelpful by design |

**The gap is the free neutral answer.** Give it away, monetise the minority who want it handled.

## Risks

- **EU261 reform has been discussed for years** — proposals have floated raising the delay threshold. Verify the current bands before building and **date every claim on the site**, the same rule that governs HowMuchOnX copy.
- **Affiliate terms unverified.** Some claim companies pay per *submitted claim*, others per *successful payout*. This swings revenue several-fold. Verify in Phase 0.
- **Incumbents are well funded** and own the head terms. Do not fight them there — take the long tail (see 03).
- **This is not legal advice.** Say so on every page, link the actual regulation, and never state eligibility as certainty.
