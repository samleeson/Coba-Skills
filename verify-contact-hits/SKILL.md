---
name: Verify Contact Hits
description: >-
  Use when you have raw contact hits (emails, phones, profiles, record entries)
  for one identity-locked person and need each confirmed, scored, and cleaned
  before delivery.
---
# Verify Contact Hits

## When
- Contact hits for one person came in from one or more searchers and need checking before anyone relies on them.

## Do
1. **Restate the identity lock.** Every hit must tie to it.
2. **Check each hit.**
   - Reopen the source URL and confirm the value appears there exactly. If the page is gone, check the Wayback Machine and note the snapshot date.
   - Confirm the source is about the locked person, not a namesake. Record the matching signals (employer, title, city, photo, cross-link).
   - Note the source date. Flag the hit as stale if the person has since changed employer or role (check their current profile and recent press).
   - Look for a second independent source. Aggregators that copy each other count as one source.
3. **Score confidence.**
   - **high:** published on a first-party page (their own site, employer site, their own profile) or in an official filing, and current.
   - **medium:** inferred and corroborated, or found in two independent sources, or first-party but older than 2 years.
   - **low:** a single inference, a single aggregator, or a stale source.
   - **rejected:** can't be found at the source, belongs to a namesake, or came from a disallowed method.
4. **Resolve conflicts.** When two values conflict, keep both, say which is more likely current, and explain why.
5. **Scrub.** Remove anything that's a home address, a family member's detail, or came from breached data, pretexting, or a login bypass, and note that it was removed.

## Output
```
Person: <name> | <employer / title / city>
Verified:
- <type>: <value>  [high|medium|low]  <source URL(s)>  <why this score>
Rejected:
- <value>  <reason>
Stale / conflicts: <notes>
```

## Never
- Upgrade a score without new evidence.
- Contact the person or send test messages to confirm a channel.
- Pass a hit that doesn't tie to the locked identity.
- Add new contact values yourself. Verification only; send gaps back to the searchers.
