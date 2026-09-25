---
name: Find Email Address
description: >-
  Use when you need the email address(es) for one identity-locked person from
  public sources: published addresses, the organization's pattern, and
  corroboration.
---
# Find Email Address

## When
- You have one person locked by name plus employer, title, or city, and need their email.
- An existing email is unsourced, stale, or only guessed.

## Do
1. **Confirm the lock.** Restate the identity (name, employer, title, city). If it's missing, stop and ask for it. Accept only evidence that ties to it.
2. **Harvest published addresses (search exhaustively).**
   - Employer site: team, bio, press, contact, careers pages; downloadable bios, press kits, annual reports, and PDFs (search `site:domain filetype:pdf "Name"`).
   - Personal site, blog, newsletter footer, portfolio, academic or lab page, CV.
   - Public code: commit author emails on public repos, package registry maintainer fields, author lines in papers and preprints.
   - Conference speaker lists, event programs, webinar pages, podcast show notes, and grant or award announcements.
   - Regulatory and nonprofit filings, board lists, and meeting minutes that list contact emails.
   - Archived versions of all of the above (Wayback Machine), especially old team and contact pages.
   - Exact-phrase searches: `"first.last@domain"`, `"Name" "@domain"`, `"Name" email`.
3. **Work out the pattern.**
   - Identify every domain the person uses (current employer, past employers, personal domain, board orgs).
   - Collect 3 or more published addresses of other people at each domain to find the format (`first.last`, `flast`, `first`, `firstl`, `f.last`, `first_last`, and so on).
   - Build candidates for the person from the confirmed format. If no format is confirmed, list the top 2–3 likely formats as unverified.
4. **Corroborate.**
   - Look up the domain's MX records (for example `dig MX domain`) to confirm it accepts mail. Flag domains with no MX record.
   - Exact-match search each candidate address. Check public directory previews that show a source.
   - Prefer an address seen in two independent places.
5. **Label each address** as `published`, `inferred – corroborated`, or `inferred – unverified`, and mark it work, personal, or role (for example info@ or press@).

## Output
```
Person: <name> | <employer / title / city>
Emails:
- <address>  [published|inferred – corroborated|inferred – unverified]  [work|personal|role]  <source URL>
Pattern evidence: <domain>: <format> (from <n> published addresses, <source URLs>)
Searched, nothing found: <sources>
```

## Never
- Present a guessed address as found, or label an inferred one as published.
- Send a test email or probe a mail server with SMTP to check an address.
- Use breached or leaked data, log in with someone else's credentials, bypass paywalls or CAPTCHAs, or pretext anyone.
- Accept a same-name address that doesn't tie to the locked identity.
