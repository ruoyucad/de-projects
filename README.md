# de-projects

Repository: https://github.com/ruoyucad/de-projects

`de-projects` is the operating workspace for finding and evaluating a small number of substantial, project-based data-engineering contracts. It is designed around selective delivery rather than high-volume freelancing: engagements of roughly two to three months, a few per year, delivered remotely from Yokohama, Japan.

## Positioning

- **Role:** Senior data engineer
- **Core work:** Data pipelines, data migration, and large-scale cleaning, deduplication, and normalization
- **Main stack:** Python, SQL, and DuckDB
- **Delivery advantage:** Heavy, disciplined use of AI coding agents for implementation and documentation, with human ownership of architecture, validation, and data-quality decisions
- **Base:** Yokohama, Japan — Japan Standard Time (JST, UTC+9)
- **Citizenship:** Canadian
- **Languages:** Chinese (native), English (fluent), Japanese (conversational, daily life only)

## Target regions

| Region | Positioning |
|---|---|
| Singapore and Hong Kong | Strong working-hours overlap with JST; suitable for regular collaboration and meetings during the business day. |
| North America | Remote delivery with partial business-hours overlap; best for projects that can operate asynchronously with a defined overlap window. |
| Other regions | Consider only when the scope, rate, and overlap requirements are explicitly workable from JST. |

Japanese-language business delivery is not currently offered. Japanese is used for daily life, not represented as business fluency.

## Channel status

| Channel | Status in this repo | Intended use | Rate posture |
|---|---|---|---|
| Braintrust | Application draft prepared; not yet submitted | Primary curated channel and first public job-board scan source | Target USD 90–100/hr within the researched USD 70–100/hr range for data roles |
| Toptal | Application draft prepared; not yet submitted | Selective channel for senior, higher-value engagements | Target USD 110–130/hr; researched senior range USD 100–175/hr |
| Arc.dev | Profile inputs available from the master profile; platform-specific draft not yet prepared | Remote-developer channel and secondary scan source | Target USD 90–120/hr |
| Direct / other boards | Scan specification prepared | Opportunistic discovery in North America, Hong Kong, and Singapore | USD 90–130/hr depending on platform, region, scope, and duration |

These statuses describe document readiness only. They do not claim that an application has been submitted or approved.

## Scan cadence plan

1. **Daily:** Run the scan in [`scan/scan-spec.md`](scan/scan-spec.md), beginning with Braintrust's public job board, followed by Arc.dev, eFinancialCareers Hong Kong/Singapore contract roles, and Wellfound remote roles.
2. **Per scan:** Save one dated output file under `leads/`, deduplicate against prior files, and rank by fit rather than posting volume.
3. **Review:** Shortlist only roles that meet the rate, contract-type, subject-matter, and timezone rules in the scan specification.
4. **No automatic applications or outreach:** A scan produces leads for review. Submission decisions remain explicit and separate.

## Repository map

- [`profile/master-profile.md`](profile/master-profile.md) — canonical facts, positioning, skills, proof points, availability, rates, and open items
- [`profile/braintrust-application.md`](profile/braintrust-application.md) — Braintrust draft answers and AI-interview preparation
- [`profile/toptal-application.md`](profile/toptal-application.md) — Toptal draft, portfolio-project description, and screening checklist
- [`scan/scan-spec.md`](scan/scan-spec.md) — daily source, filter, scoring, output, and deduplication rules
- `leads/` — dated scan outputs; initially empty

## Non-negotiable accuracy rules

- Do not add employers, clients, dates, years of experience, certifications, tools, or portfolio links that are not present in the master profile.
- Do not describe Japanese as business-fluent.
- Do not treat the financial-institution contract as a named reference or public case study unless Qian explicitly approves that use.
- Contracting entity and cross-border tax structuring remain open items for Qian and his tax advisor. Platform or Contractor-of-Record arrangements must be confirmed for each engagement.
