---
name: Transcript Healthcheck
description: >-
  Use when auditing Grok Bot fleet transcripts for user friction, proposing new
  skills/bots/routines from repeated corrections, or running the standing
  transcript-healthcheck routine.
---
# Transcript Healthcheck

## When

- The standing `transcript-healthcheck` routine fires
- The user asks for a fleet checkup, friction audit, or “what should we automate”
- First run after this skill is imported (offer cadence then)

## Do

1. Set the window: default last 24 hours, or the cadence named by the routine/user. State the window and bot count before mining.
2. Build the corpus on this computer:
   - `/home/box/agent-data/agent-transcripts/<agentId>/<agentId>.jsonl`
   - skip folders whose names start with `sand-subagent-`
   - order candidates by real modification time, never by UUID name
   - map `<agentId>` to a name via `/home/box/agent-data/agents/<agentId>/profile.json`
3. Fan out parallel subagents (recall-shaped). Each gets a slice of agent transcript paths. The main thread keeps only their findings.
4. Each subagent returns one block per bot that had user traffic in the window:
   - bot name and id
   - user goals in the window (short)
   - friction signals with short quotes or paraphrases (cite approx turn or timestamp if present)
   - repeated corrections or re-asks
   - misunderstandings (bot did X, user wanted Y)
   - candidate gaps: skill / bot / routine, one line each, or `none`
5. Look for friction: frustration, sarcasm, “stop”, “wrong”, “i said”, “undo”, “not what i meant”; same instruction restated; user doing work the bot should own; bot asking preference questions an experiment could settle; quiet failure (user abandons a thread).
6. Skip bots with no user messages in the window. Null is a finding.
7. On first import, ask once what cadence they want (default weekday morning). Create or update the standing routine named `transcript-healthcheck` to match. Do not ask again every run.

## Output

Capsule (at most 5 bullets), then a short list of proposals each tagged `skill` | `bot` | `routine` with the evidence line that earned it, then “no change” bots in one line if useful. Stay quiet when the routine fires and there is nothing to propose — do not send “(no change.)”. Offer to implement only after the user picks.

## Never

- CreateAgent, write skills, or create routines from this report alone
- Send “(no change.)” on an empty routine wake
- Re-ask cadence every run after first import
