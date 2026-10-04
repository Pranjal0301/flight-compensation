# 06 — Revenue Projections

**All figures modelled, not measured.** Dated 2026-09-26.

## Streams, in order of activation

1. **Claim-service referral** (day 1) — $20–60 per converted claim. The thesis.
2. **Travel insurance affiliate** (month 2+) — natural adjacency; someone who just lost a day to a delay is receptive
3. **Display ads** (month 4+, past 10k sessions) — guide pages only
4. **Paid API** (month 6+) — travel apps, corporate travel tools, insurers who want to surface entitlements

## The model

```
monthly_revenue = visits x eligible_rate x referral_conversion x payout
                + pageviews x rpm / 1000
```

Assumptions: ~15–25% of visitors have a genuinely eligible claim (most people checking were in fact delayed); of those, 3–8% hand it to a paid service rather than claim free.

| Month | Visits/mo | Referrals | Referral rev | Ads | **Total/mo** |
|---|---|---|---|---|---|
| M1 (Nov) | 600 | 2–5 | $40–200 | $0 | **$40–200** |
| M3 (Jan) | 3,000 | 9–24 | $180–960 | $0 | **$180–960** |
| M6 (Apr) | 10,000 | 30–80 | $600–3,200 | $50 | **$650–1,600** |
| M12 (Nov 2027) | 25,000 | 75–200 | $1,500–8,000 | $150 | **$1,650–3,000** |

Conservative read: **$300–2,000/mo at month 12.** The upper end of the raw model is optimistic — I have trimmed the headline range because referral conversion on a site that also gives away a free letter will realistically sit at the low end. That trade is deliberate: the free letter is what earns the links that make the traffic possible.

## Seasonality

This is **not** a flat curve. Summer ATC strikes and winter weather disruption produce spikes of several times baseline. A single bad week across European aviation can outperform a normal month.

Practical consequence: **build content before the season.** Traffic arrives the day disruption hits, not the week after.

## Costs

| Item | Monthly |
|---|---|
| Domain | ~$1 (plus ~$1 if you take the .co.uk) |
| Vercel | $0 |
| Data | $0 — bundled, static |
| **Total** | **~$1–2** |

**The cheapest site in the portfolio to operate.** No API, no database, no cron, no vendor. Once built, it costs essentially nothing to leave running for years, which is exactly why it is worth building even at the low end of the range.

## The honest downside

The incumbents are well funded and own the head terms. If they also dominate the long tail — route pages, objection queries — the traffic model fails and this lands nearer $300/mo than $2,000.

Even then it stays profitable, because it costs $12/yr. That asymmetry is the argument for building it regardless of where in the range it lands.
