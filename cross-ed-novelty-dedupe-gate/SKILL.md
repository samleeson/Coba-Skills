---
name: Cross-ED novelty dedupe gate
description: >-
  Use when Hunter ED scouts or the Hunter orchestrator claim NEW candidates
  across ED1–ED8: check other ED packs first and drop or flag cross-ED
  duplicates before handoff.
---
# Cross-ED novelty / dedupe gate

Use before any Hunter ED scout (or Hunter orchestrator) delivers a “new” candidate list across COBA ED1–ED8.

## Rule

A person already claimed in another ED’s current pack is **not new**. Claiming “exactly N NEW” requires a cross-ED check, not only within this ED file.

## Before handoff

1. Build a name set from all other live ED packs under the shared workspace (or the orchestrator’s combined rollup / claimed list).
2. Normalize names (case-fold; strip titles like “Dr.”).
3. Drop or re-label any candidate already present in another ED as `cross-ED duplicate (see EDn)` — do not count them toward the NEW quota.
4. Only then fill the NEW quota with true novelties. If you cannot find enough true new people, ship fewer and say so — never pad with dupes.
5. Orchestrator pre-handoff: run the same gate across all eight before telling the user the swarm is done.

## Never

- Treat “new to this ED file” as “new to the fleet.”
- Quietly leave the same person in two EDs under different confidence labels without marking the duplicate.
