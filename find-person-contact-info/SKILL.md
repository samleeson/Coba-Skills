---
name: Find Person Contact Info
description: >-
  Use when asked to find email, phone, social, or other contact channels for a
  specific named person from public sources.
---
# Find Person Contact Info

## When

- Asked for contact information on a specific named person
- Need one or more reach channels: email, phone, professional profile, social handle, personal site, booking link
- Enriching or re-checking a contact entry that is sparse, stale, or unsourced

## Do

### 1. Lock identity

1. Collect every disambiguator available: full name, employer, title, city or region, school, prior employers, known profile URLs.
2. Search the name with those disambiguators and build a one-line identity lock (for example: name, employer, title, city).
3. If the name is common and nothing disambiguates it, return 2–3 candidates with distinguishing facts and ask which one before continuing.
4. From here on, only accept evidence that ties to the locked identity. Discard same-name results.

### 2. Search every channel

Work each channel until it is exhausted. Do not stop at the first hit. Run independent lookups in parallel. Record every hit with its source URL.

**Professional presence**
- Professional networking profile: URL, headline, employer, location, any visible contact fields.
- Employer website: team, about, leadership, press, contact pages, downloadable bios.
- Speaker pages for conferences, podcasts, webinars, and panels.
- Personal site, blog, newsletter, code repositories, portfolio, or academic page: footer, contact page, mailto links.
- Press coverage, bylines, and author pages.

**Email**
1. Collect any address published verbatim (employer site, bios, PDFs, press kits, personal site, public code commits, event listings).
2. Identify the employer or personal domain.
3. Find the organization's address format from other employees' published addresses; if none, enumerate common formats (`first`, `first.last`, `flast`, `firstl`, `f.last`, `first_last`, `last`).
4. Corroborate candidate addresses with exact-match searches and public directory entries that show a source.
5. Label each address: `published`, `inferred – corroborated`, or `inferred – unverified`.

**Phone**
- Organization main line from its contact page (label it as an organization line).
- Direct lines only where published in a bio, press kit, filing, or directory that names the person.
- Mobile numbers only where the person or their organization published them.

**Social and messaging**
- Public profiles on major social platforms, accepted only when the bio or content ties to the locked identity.
- Public scheduling or booking links.
- Messaging handles only when the person published them.

**Records, directories, archives**
- Public regulatory and corporate filings that list officers or contacts.
- Business entity registries.
- Nonprofit filings listing officers.
- Professional association and alumni directories.
- Free public previews on people-search and business-contact directories; treat as leads until confirmed by another source.
- Web archive snapshots of old team, bio, or contact pages.
- Domain registration records, only to confirm who owns a domain.

### 3. Verify and score

For each hit:
1. Reopen the source and confirm the value appears there.
2. Confirm the source ties to the locked identity.
3. Note the date and flag it if the person appears to have changed roles.
4. Look for a second independent source.
5. Score confidence:
   - **high**: published on a first-party page or official filing
   - **medium**: inferred and corroborated, or found in two independent directories
   - **low**: single inference or single aggregator
6. When two values conflict, keep both, state which is more likely current, and why.

### 4. Deliver

```
Person: <full name>
Identity: <employer / title / location>
Contacts:
- <type>: <value>  [high|medium|low]  <source URL>
Gaps: <channels searched with no result>
Not retrieved: <leads behind a login or paywall>
```

If nothing usable is found, say so and list what was searched.

## Output

One contact card per identity-locked person: every channel with a value, confidence, and source URL, plus explicit gaps.

## Never

- Invent or guess a contact value and present it as found
- Label an inferred email as published
- Accept a same-name result without tying it to the locked identity
- Contact the person to test a channel (no test emails, calls, or messages)
- Bypass logins, paywalls, or CAPTCHAs, or use breached data, phishing, or pretexting
- Drift into biography, analysis, or outreach writing; contact channels only
- Stop early while major channels remain unchecked
