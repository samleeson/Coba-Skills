---
name: Deep Verify ED Swarm
description: >-
  Use when the user asks for a deep verify of COBA ED1–ED8 research: fan out to
  ED1–ED8 specialist reviewers, then synthesize — do not re-scout.
---
# Deep Verify ED Swarm

## When

- User asks for a deep verify / deep review of COBA ED1–ED8 investor research
- ED-specialist reviewer bots already exist
- Ask is a deep verify across domains (not a single-claim check)

## Do

1. Confirm the ask is a deep verify across domains (not a single-claim check).
2. Fan out to the ED-specialist reviewers (ED1–ED8), one domain each, with the matching Hunter ED source path or paste.
3. Each specialist: verify claims, add material context, apply the citation bar (`Person — URL`), return a domain review.
4. Parent Reviewer synthesizes only after all domain reviews return: cross-domain conflicts, shared gaps, ranked fixes.
5. Hand the domain reviews + synthesis to merge (or the user) for expand-in-place rewrites; attach individual EDs.

## Output

Eight domain reviews plus a parent synthesis (conflicts, shared gaps, ranked fixes); individual EDs attached for merge/expand-in-place.

## Never

- Re-scout leads (Hunter’s job)
- Collapse eight domains into one thin summary before specialists finish
- Skip the citation bar on any domain review
- Create new ED-clone bots if the eight already exist — message the existing ones
