---
name: Run Contact Team
description: >-
  Use when orchestrating contact-finding for one or more named people: lock
  identity, fan out email, phone and social, and records searches in parallel,
  verify, and deliver sourced contact cards.
---
# Run Contact Team

## When
- You are handed a list of named people and need verified contact cards for each.
- You coordinate specialist searchers (agents or workers), or play every role yourself when none exist.

## Do
1. **Lock each identity.** For every person, write a one-line lock (name, employer, title, city) from what the requester gave plus a quick search. If a name is ambiguous, return 2–3 candidates with distinguishing facts and ask which one before searching.
2. **Fan out in parallel.** Give each person's lock to three searches at once:
   - email, following the Find Email Address skill
   - phone and social, following the Find Phone and Social skill
   - records and archives, following the Dig Public Records for Contacts skill
   If you have no specialists, run the three yourself, one after another.
3. **Push for thoroughness.** When a search comes back, check it against its skill's source list. Send it back once, naming the unchecked sources, if major ones were skipped or it stopped at the first hit.
4. **Verify.** Pass the combined hits through the Verify Contact Hits skill. Send any rejected or low-confidence hits that matter back to the right searcher for a second look, one round only.
5. **Assemble the card.** Merge the verified hits and dedupe them. Order each channel best first: high confidence, then direct over org line, then work over personal.
6. **Deliver.** Send one card per person to the requester. Name the gaps honestly.

## Output
```
Person: <full name>
Identity: <employer / title / location>
Best route: <single best channel and why>
Contacts:
- <type>: <value>  [high|medium|low]  <source URL>
Gaps: <channels searched with no result>
Not retrieved: <leads behind a login or paywall>
```

## Never
- Deliver a hit that didn't pass verification, or present an inference as published.
- Contact the person, send test messages, or write outreach.
- Use or allow breached data, pretexting, fake accounts, or login, paywall, or CAPTCHA bypasses.
- Include home addresses, family details, or information about minors.
- Drift into biography or analysis. Deliver contact channels only.
