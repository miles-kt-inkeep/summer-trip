---
title: Work Log
description: Append-only audit trail. After each turn that creates, edits, or restructures content in the knowledge base, append one dated entry here (one per turn, not per file). Silent edits break the audit trail.
---
# Work Logs

Append-only audit trail. **Append a dated entry after any turn that creates, edits, or restructures content in the knowledge base.** One entry per turn, not per file. Silent edits break the chain that makes knowledge-base changes auditable.

What to log:

- `ingest` runs (new external sources captured)
- `research` / `consolidate` runs (provisional or canonical articles produced)
- Direct `write_document` / `edit_document` / renames / deletions outside the three Karpathy-layer tools (`ingest` / `research` / `consolidate`)
- `discover` runs (project conventions extracted; folder frontmatter / templates / `.okignore` proposals applied; link-graph activations)
- Folder restructures (`ok seed`, manual reorganization)
- `.ok/config.yml` changes.

**Reference docs as markdown links, not bare paths.** Every doc you touched should appear as `[path/to/doc](./path/to/doc.md)` so the log shows up in `links({ kind: "backlinks" })` for those docs. A bare path string (`Files touched: foo/bar.md`) does not register in the doc graph. The audit trail compounds only when the log is a real linker.

<!-- Example entry shape:

## YYYY-MM-DD: <short title>

- <what was done>
- Files touched: [path/to/doc-a](./path/to/doc-a.md), [path/to/doc-b](./path/to/doc-b.md)
- Sources ingested: [source-slug](./external-sources/source-slug.md)
- Open follow-ups: <topic-1>, <topic-2>

\-->

## 2026-06-02: August trip research — surf vs. multi-day hike

- Researched and proposed options for a \~1-week August trip (group of 2–4, NYC + SF, mid budget, advancing-beginner surfers / experienced hikers, optional city finish).
- Captured 7 external sources: [hike-tour-des-combins](./external-sources/hike-tour-des-combins.md), [hike-berliner-hoehenweg](./external-sources/hike-berliner-hoehenweg.md), [hike-alta-via-1-dolomites](./external-sources/hike-alta-via-1-dolomites.md), [surf-where-to-surf-august](./external-sources/surf-where-to-surf-august.md), [surf-costa-rica-seasons](./external-sources/surf-costa-rica-seasons.md), [surf-ericeira-camps](./external-sources/surf-ericeira-camps.md), [logistics-flights-august](./external-sources/logistics-flights-august.md).
- Wrote 2 research syntheses: [surf-trip-options](./research/surf-trip-options.md), [alpine-hike-options](./research/alpine-hike-options.md).
- Wrote 6 trip proposals: [00-overview-surf-vs-hike](./trips/00-overview-surf-vs-hike.md), [surf-portugal-ericeira](./trips/surf-portugal-ericeira.md), [surf-costa-rica-nosara](./trips/surf-costa-rica-nosara.md), [hike-alta-via-1-dolomites](./trips/hike-alta-via-1-dolomites.md), [hike-tour-des-combins](./trips/hike-tour-des-combins.md), [hike-berliner-hoehenweg](./trips/hike-berliner-hoehenweg.md).
- Note: trip docs tagged `status: proposal` (pre-decision) rather than the template's `status: canonical`; promote the chosen one via consolidate once the team decides.
- Open follow-ups: lock August dates + pull live airfares; book perishable items (surf-camp slots / Alta Via 1 rifugios); confirm group comfort with Berliner Höhenweg exposure.

## 2026-06-02: Surf follow-up — non-camp / independent options

- Followed up on surf request: non-camp options where you book your own lodging + take 1–2 à-la-carte lessons.
- Captured 2 external sources: [surf-independent-lessons-rentals](./external-sources/surf-independent-lessons-rentals.md), [surf-san-sebastian](./external-sources/surf-san-sebastian.md).
- Wrote research synthesis [surf-independent-and-city-surf](./research/surf-independent-and-city-surf.md) (DIY pricing model + San Sebastián as city-is-the-base option).
- Added proposal [surf-san-sebastian-independent](./trips/surf-san-sebastian-independent.md); added "Independent (non-camp) variant" sections to [surf-portugal-ericeira](./trips/surf-portugal-ericeira.md) and [surf-costa-rica-nosara](./trips/surf-costa-rica-nosara.md); updated [00-overview-surf-vs-hike](./trips/00-overview-surf-vs-hike.md) (new row, recommendation, flowchart).
- Open follow-ups: San Sebastián vs Ericeira as lead DIY pick; pre-book August lessons vs arrange on arrival; shared Airbnb sizing for 2–4.

## 2026-06-02: Concrete mid-August flight examples

- Added concrete flight examples (depart Sat Aug 15 → Sat Aug 22, 2026) avoiding long/multi-stop layovers, for all surf + hike gateways from NYC and SF.
- Captured external source [logistics-flight-routings](./external-sources/logistics-flight-routings.md) (carrier/route/nonstop facts) and wrote research doc [flight-examples-mid-august](./research/flight-examples-mid-august.md) (dated example itineraries + meet-up notes).
- Added "Getting there (mid-Aug example)" callouts to all six proposals: [surf-portugal-ericeira](./trips/surf-portugal-ericeira.md), [surf-san-sebastian-independent](./trips/surf-san-sebastian-independent.md), [surf-costa-rica-nosara](./trips/surf-costa-rica-nosara.md), [hike-alta-via-1-dolomites](./trips/hike-alta-via-1-dolomites.md), [hike-tour-des-combins](./trips/hike-tour-des-combins.md), [hike-berliner-hoehenweg](./trips/hike-berliner-hoehenweg.md); linked flight examples from [00-overview-surf-vs-hike](./trips/00-overview-surf-vs-hike.md).
- Key finding: from NYC nearly every gateway is a nonstop; from SF take one well-chosen connection (Newark→Lisbon, Madrid→Bilbao, Zurich→Geneva). SF→Munich and SF→Liberia are nonstop.
- Open follow-ups: pull live fares for the locked week; verify SFO→LIR and summer SWISS JFK→GVA frequency; decide whether SF folks connect via Newark to share the NYC transatlantic leg.

## 2026-06-02: Surf camp comparison (Portugal / Spain / Costa Rica)

- Researched and compared specific named surf camps across the three regions; captured the bundle-vs-à-la-carte distinction.
- Captured external source [surf-camp-options](./external-sources/surf-camp-options.md) (per-camp offerings + pricing: Lapoint, Rapture, Ericeira Surf Camp, Good People, Stoke, Zarautz Surf House, Dreamsea, Lapoint CR, Safari Surf).
- Wrote new comparison page [surf-camp-comparison](./research/surf-camp-comparison.md) with per-country tables, a value chart, and a group-tuned recommendation (Good People Zarautz à-la-carte for improvers; Dreamsea best-value bundle; Lapoint most polished).
- Cross-linked it from [surf-portugal-ericeira](./trips/surf-portugal-ericeira.md), [surf-san-sebastian-independent](./trips/surf-san-sebastian-independent.md), [surf-costa-rica-nosara](./trips/surf-costa-rica-nosara.md), and [00-overview-surf-vs-hike](./trips/00-overview-surf-vs-hike.md).
- Open follow-ups: confirm Good People August dates + lesson-pack price; bundle vs à-la-carte group decision; dorm vs private room; CR base (Tamarindo/Santa Teresa/Nosara).

## 2026-06-02: August surf conditions by spot

- Researched August-specific surf conditions (wave size, water temp, wind, consistency, crowds) for Ericeira, Zarautz/San Sebastián, Nosara, Santa Teresa, Tamarindo.
- Captured external source [surf-conditions-august](./external-sources/surf-conditions-august.md) and wrote research page [surf-conditions-august](./research/surf-conditions-august.md) with a side-by-side table, decision flowchart, and morning-surf rule.
- Key finding: Costa Rica is peak season / most consistent (29–30 °C, glassy AM offshore; Santa Teresa punchiest); Ericeira gentlest but smaller + colder (Nortada, wetsuit, AM only); San Sebastián riskiest for flat days (summer = flat season).
- Threaded "August conditions" notes into [surf-portugal-ericeira](./trips/surf-portugal-ericeira.md), [surf-san-sebastian-independent](./trips/surf-san-sebastian-independent.md), [surf-costa-rica-nosara](./trips/surf-costa-rica-nosara.md); linked from [00-overview-surf-vs-hike](./trips/00-overview-surf-vs-hike.md) and [surf-camp-comparison](./research/surf-camp-comparison.md).
- Note: edit\_document returned a spurious frontmatter-intersect error on one parallel edit; succeeded on retry.
- Open follow-ups: check live forecasts \~10 days out once dates lock; confirm flat-day backup spots (Ericeira breaks; Mundaka/Sopelana from San Sebastián).

