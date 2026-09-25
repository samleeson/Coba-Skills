---
name: Dig Public Records for Contacts
description: >-
  Use when you need contact channels for one identity-locked person from public
  records, filings, directories, and web archives.
---
# Dig Public Records for Contacts

## When
- You have one person locked by name plus employer, title, or city, and need contact channels that come from records, directories, or archives rather than profiles.

## Do
1. **Confirm the lock.** Restate the identity. If it's missing, stop and ask. Accept only records that tie to it.
2. **Business and securities records.**
   - State business-entity registries: entities where they are an officer, manager, or registered agent, with the business addresses and contacts on file.
   - SEC EDGAR: Form D, Form ADV (advisers), 13F, proxy statements, and 8-Ks listing them, with the business contact info in each filing.
   - FINRA BrokerCheck and IAPD for registered representatives and advisers.
3. **Nonprofit and civic records.**
   - IRS Form 990s (via ProPublica Nonprofit Explorer or Candid previews) listing them as an officer, director, or key employee.
   - Board and commission rosters, city and state appointment lists, and meeting minutes.
4. **Professional and court records.**
   - State professional licensing boards (law, medicine, real estate, CPA, contractor) for business contact info on the license.
   - Bar directories, medical board lookups, and professional association and alumni directories.
   - Court dockets (PACER index, state portals) only for business contact info on filings where they are counsel or a corporate party.
5. **Web infrastructure and archives.**
   - WHOIS and historical registration records to confirm who owns a personal or business domain and any business contact published there.
   - Wayback Machine snapshots of old team, bio, and contact pages, and of their personal site.
   - Google cache and search-engine snippets for pages that have since been removed.
6. **Directory previews.** Free public previews on business-contact and people-search directories count as leads only. Confirm each one with a first-party source before reporting it as confirmed.

## Output
```
Person: <name> | <employer / title / city>
Record hits:
- <record type>: <contact value>  <record URL>  <record date>
Leads needing confirmation:
- <value>  <directory>  <URL>
Searched, nothing found: <registries and archives>
```

## Never
- Report home addresses, date of birth, relatives, or other personal identifiers. Stick to business and professional contact channels.
- Buy or use background-check reports, breached data, or paid records obtained by logging in as someone else.
- Bypass paywalls, CAPTCHAs, or access controls.
- Treat a directory preview as confirmed without a first-party source.
