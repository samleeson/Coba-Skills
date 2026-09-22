# Universal SKILL.md format

Every skill under this repo (and its live copy in `/home/box/agent-data/workflows/<slug>/SKILL.md`) uses the same shape.

```markdown
---
name: <Human Title Case Name>
description: >-
  Use when <one clear trigger line>. Keep under ~200 chars if possible.
---
# <Same Human Title>

## When
- 2–5 bullets: when to run this skill

## Do
Numbered steps (### subsections OK for long procedures).

## Output
What the deliverable looks like (short). Prefer a one-liner for gates.

## Never
- Anti-patterns as bullets
```

Rules: preserve all substantive content; description starts with “Use when” / “Use before”; same folder slugs; no assistant-specific Slack/repos unless intrinsic to the skill (COBA/ED paths OK).
