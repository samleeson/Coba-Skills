---
name: Find Phone and Social
description: >-
  Use when you need published phone numbers, social profiles, messaging handles,
  or booking links for one identity-locked person from public sources.
---
# Find Phone and Social

## When
- You have one person locked by name plus employer, title, or city, and need phone numbers or social and messaging channels.

## Do
1. **Confirm the lock.** Restate the identity. If it's missing, stop and ask. Accept only evidence that ties to it.
2. **Phone (published only).**
   - Organization main line, office or branch line, and assistant or executive-office line from contact and leadership pages.
   - Direct lines printed in bios, press releases (media-contact blocks), speaker kits, filings, licensing records, or association directories.
   - Mobile numbers only where the person or their organization published them (email signatures posted publicly, personal site, business listings).
   - Label each number as `org line`, `direct`, `assistant`, or `mobile`, and give the page it came from.
3. **Social profiles.** Check every major platform: professional networking, X, Instagram, Facebook (public pages), Threads, Bluesky, YouTube, TikTok, Substack/Medium, GitHub, and any niche platform for their field.
   - Search the name plus disambiguators on each platform and in search engines (`site:platform.com "Name" "Employer"`).
   - Follow outbound links from the personal site, employer bio, podcast pages, and speaker bios; these are the strongest leads.
   - Tie each profile to the locked identity with at least two matches (same headshot, employer, title, city, cross-links, or consistent posting history). Record which matches you used.
4. **Messaging and booking.** Collect public scheduling links (Calendly and similar), contact forms, and messaging handles (Signal, WhatsApp, Telegram) only where the person published them.
5. **Media and speaking contacts.** Note agents, publicists, or speaker bureaus listed as the route to the person.

## Output
```
Person: <name> | <employer / title / city>
Phones:
- <number>  [org line|direct|assistant|mobile]  <source URL>
Social:
- <platform>: <URL/handle>  matched on: <signals>  <source URL>
Messaging / booking / reps:
- <type>: <value>  <source URL>
Searched, nothing found: <platforms and sources>
```

## Never
- Call, text, message, follow, or friend-request the person to test a channel.
- Use unpublished personal numbers from leaked data, carrier lookups, or pretexting.
- Log in as someone else, create fake accounts, or get past privacy settings on private profiles.
- Collect home addresses or details about family members or minors.
- Accept a same-name profile without two matching signals.
