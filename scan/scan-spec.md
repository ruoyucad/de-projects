# Daily Contract Scan Specification

## Purpose

Find a small number of high-fit, project-based data-engineering contracts for review. The scan is a lead-generation process only: it must not submit applications, send outreach, create accounts, or bypass login, paywall, or access controls.

## Operator profile

- Senior data engineer based in Yokohama, Japan (JST, UTC+9)
- Canadian citizen
- Core fit: data pipelines, data migration, large-scale data cleaning, deduplication, and normalization
- Core stack: Python, SQL, DuckDB
- Professional languages: English and Chinese
- Japanese: daily-life conversation only; exclude roles requiring business Japanese
- Preferred engagement: remote contract/freelance project lasting two to three months
- Volume goal: a few substantial engagements per year, not maximum lead volume

## Cadence and output location

- **Frequency:** Daily
- **Suggested run time:** 08:30 JST
- **Output:** One Markdown file per run at `leads/YYYY-MM-DD.md`
- **Timezone for deadlines:** Preserve the deadline and timezone exactly as shown in the source; add a JST conversion only when it can be calculated unambiguously.

## Source order

### 1. Braintrust public job board — first

- Search the public job board before all other sources.
- Use combinations of: `data engineer`, `data engineering`, `data migration`, `ETL`, `data pipelines`, `Python`, `SQL`, and `contract`.
- Prefer direct role pages that expose employer, engagement type, duration, location/remote rules, and rate.

### 2. Arc.dev

- Search remote data-engineering and data-migration roles.
- Capture whether the role is contract, freelance, or contract-to-hire. Exclude permanent roles unless the listing explicitly offers a contract option.

### 3. eFinancialCareers — Hong Kong and Singapore

- Search contract data-engineering roles in Hong Kong and Singapore.
- Suggested terms: `data engineer contract`, `data migration contract`, `ETL contract`, `Python SQL contract`, and `data platform contract`.
- Record the employer's remote policy exactly. A Hong Kong or Singapore location is not sufficient if the role requires local on-site attendance or local work authorization that has not been confirmed.

### 4. Wellfound remote

- Search remote data-engineering roles and contract-friendly startups.
- Treat missing rate, duration, or contracting details as unknowns to verify, not as passes.

### Additional sources

Do not add a source merely because it has volume. A new source must provide direct role pages, meaningful contract roles in the target regions, and enough information to apply the filters below.

## Search concepts

Include roles whose primary work matches one or more of:

- Data engineering
- Data pipelines / ETL / ELT
- Data migration
- Data platform data layer
- Data quality remediation
- Data cleaning
- Deduplication / entity normalization
- Analytical dataset construction

Exclude roles that are primarily:

- Data science, machine-learning research, or model development
- Analytics reporting or dashboard production with no engineering component
- Data entry or manual data cleaning
- Database administration only
- Data governance, compliance, or programme management only
- Permanent employment with no contract/project option
- Business-Japanese delivery
- On-site work outside Japan

## Hard filters

A lead can be shortlisted only if the available evidence supports all of the following:

| Filter | Rule |
|---|---|
| Subject | Primary responsibility is data engineering, pipelines, migration, or large-scale data processing |
| Engagement type | Contract, freelance, project-based, or explicitly contract-friendly |
| Duration | Two to three months preferred; a different duration may be marked `REVIEW` only if the scope is project-based and the rate is strong |
| Location | Fully remote, or remote from Japan/APAC under the listing's stated rules |
| Region | North America, Hong Kong, or Singapore; other regions require an explicit remote-from-Japan policy |
| Rate | At least USD 70/hr equivalent where a rate is published; unknown rate is `VERIFY`, not a pass |
| Language | English-language delivery; no business-Japanese requirement |
| Access | Publicly visible listing or a source Qian has authorized KiKi to access |

## Timezone-overlap rule

Use 09:00–18:00 JST as the default collaboration window for comparison unless Qian sets a project-specific alternative.

- Calculate overlap against the client's stated core hours when available.
- **Preferred:** At least three hours of overlap with JST business hours.
- **Acceptable for review:** Less than three hours if the listing is strongly asynchronous and meetings are limited to a defined window.
- **Flag, do not silently reject:** North American roles with no stated core hours; record `timezone requirement unknown`.
- Hong Kong and Singapore normally provide strong overlap because they are one hour behind JST.

## Scoring

Score only after the hard-filter check.

| Signal | Points |
|---|---:|
| Explicit two-to-three-month duration | +3 |
| Published rate at or above USD 90/hr equivalent | +3 |
| Published rate USD 70–89/hr equivalent | +1 |
| Migration, dedup, normalization, or data-quality work is central | +3 |
| Python and SQL are central | +2 |
| DuckDB or analytical file-based processing is relevant | +1 |
| Hong Kong or Singapore remote with strong JST overlap | +2 |
| North America remote with at least three hours' stated overlap or clear async process | +1 |
| Direct, detailed role page with named client and clear scope | +1 |
| Rate missing | −1 |
| Duration missing | −1 |
| Remote eligibility from Japan unclear | −2 |
| Contract-to-hire emphasis | −2 |

### Priority labels

- **A — Shortlist:** Passes hard filters and scores 8 or higher
- **B — Review:** Passes most hard filters, scores 5–7, or has one material unknown
- **C — Watch:** Relevant but weak on rate, duration, timezone, or eligibility
- **Excluded:** Fails a hard filter; do not include in the main lead table, but count it in the run summary

## Rate normalization

- Preserve the original rate, currency, unit, and contract terms exactly as published.
- Add an approximate USD/hour equivalent only when the source gives enough information to calculate it.
- For monthly rates, state the assumed working hours used in the conversion. If no defensible assumption is available, do not convert.
- Do not treat equity, bonuses, or benefits as part of the contract hourly rate.

## Output format

Each `leads/YYYY-MM-DD.md` file must use this structure:

```markdown
# Contract Scan — YYYY-MM-DD

## Run summary

- Scan time (JST):
- Sources checked:
- Listings inspected:
- New leads:
- Updated leads:
- Duplicates merged:
- Excluded by hard filters:
- A / B / C counts:

## A — Shortlist

| Score | Role | Company | Source | Region / remote rule | Type / duration | Published rate | USD/hr equiv. | Timezone overlap | Deadline | URL | First seen |
|---:|---|---|---|---|---|---:|---|---:|---|---|---|

### A1. [Role title] — [Company]

- **Source:**
- **URL:**
- **Location / remote eligibility:**
- **Engagement type and duration:**
- **Published rate:**
- **Core work:**
- **Stack named in listing:**
- **Timezone / core hours:**
- **Why it fits:**
- **Unknowns or risks:**
- **Next action:** Review only / verify rate / verify eligibility / prepare application

## B — Review

[Repeat the same table and detail-block format.]

## C — Watch

[Repeat the same table and detail-block format.]

## Source notes

- Access problems, missing fields, changed pages, or other observations that affect future scans.
```

If there are no leads in a priority band, write `None found in this run.` under that heading rather than omitting the band.

## Deduplication rule

Deduplication is mandatory across sources and across days.

1. **Canonical URL:** Remove tracking parameters and fragments; normalize trailing slashes and obvious URL casing differences.
2. **Primary key:** Canonical role URL.
3. **Cross-source key:** Normalized combination of:
   - Company name (lowercase; remove punctuation and legal suffixes)
   - Role title (lowercase; normalize seniority and punctuation)
   - Region / remote rule
   - Core role identifier or requisition ID, when published
4. If the primary or cross-source key matches an earlier lead, merge source names and URLs into the existing record rather than creating a new lead.
5. Preserve `first_seen`; update `last_seen`, rate, duration, deadline, and status when the source changes.
6. Resurface a previously reported lead only when a material field changes: rate, duration, remote eligibility, deadline, role status, or a corrected URL.
7. Near-duplicates that cannot be merged confidently must be marked `possible duplicate` and linked to the suspected earlier lead instead of being counted as new.
8. Closed or expired roles remain in the historical file with status `Closed`; do not delete the audit trail.

## Status vocabulary

- `New`
- `Updated`
- `Reviewing`
- `Shortlisted`
- `Applied`
- `Rejected`
- `Closed`
- `Possible duplicate`

Only Qian or an explicitly authorized workflow may change a lead to `Applied`.

## Quality rules

- Quote role requirements from the listing; do not infer a duration, rate, or remote rule that is not stated.
- Keep unknowns visible in the detail block.
- Prefer ten well-evidenced leads over a long, weakly filtered list.
- Record source access failures in `Source notes`; do not replace missing evidence with search-result snippets alone when a direct role page is available.
- Never store credentials, passport details, tax information, bank details, or private application documents in `leads/`.
