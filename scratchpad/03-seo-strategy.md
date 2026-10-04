# 03 — SEO + AEO Strategy

Incumbents are well funded and own the head terms. **Do not fight them there.** The entire strategy is the long tail they will never write.

## Keyword targets

**Head terms — do not target directly (AirHelp et al. own these):**
- "flight delay compensation", "EU261"

**Programmatic route pages — the volume engine:**
- `/route/lhr-jfk` → "LHR to JFK delayed? You could be owed £520"
- Every major route has a real, different compensation figure. That is genuine unique substance per page, not a template swap.
- Hundreds of airlines x thousands of routes. Seed the top few hundred; expand as they index.

**Per-airline pages:**
- "[airline] delay compensation" · "[airline] claim process"
- How that carrier handles claims, what they typically argue, which authority regulates them

**Long-tail question pages (where the traffic actually is):**
- "flight delayed 3 hours compensation"
- "can I claim if the delay was weather"  ← the single most-searched objection
- "how long do I have to claim flight compensation"
- "connecting flight missed compensation"
- "is my flight delay extraordinary circumstances"

## Programmatic rules

Same discipline as x-revenue:

1. **Unique substance per page** — actual distance, actual band, that route's typical delay profile, that airline's claim address. Not a template with the airport code swapped.
2. **Seed a few hundred routes, not thousands.** Watch GSC coverage before scaling.
3. Internal linking: route → airline → guide → checker.
4. Noindex routes that do not qualify for anything.

## Technical checklist

- Fully static build; every page prerendered
- Sitemap split by section (routes, airlines, guides)
- `FAQPage` JSON-LD on guides, `SoftwareApplication` on the checker
- OG image per route ("LHR to JFK — up to £520 if delayed 3h+")
- Fast LCP; this is a mobile-first audience sitting in an airport

## AEO — unusually strong fit here

People ask assistants this question constantly, in exactly this shape: *"my flight was delayed 4 hours, am I owed anything?"*

- **Methodology page** with dated, quotable rules: "As of September 2026, EU261 sets compensation at €250 / €400 / €600 by distance band…"
- **`llms.txt`** documenting the rules and the `/api/check` endpoint
- **Allow AI crawlers.** A cited answer here is a visitor with a live claim.
- Plain Q&A blocks everywhere

## Distribution

1. **r/flying, r/travel, r/unitedkingdom, r/europetravel** — people post delay stories constantly; a free checker is genuinely welcome
2. **Seasonal spikes are the unlock** — summer ATC strikes, winter weather chaos. Have the content ready *before* the disruption, not after.
3. Travel bloggers and consumer journalists need a free tool to link to
4. The free claim-letter generator is the natural link magnet — nobody else gives it away
