# Braintrust Application Draft

**Status:** Ready-to-review draft; not yet submitted.  
**Source of facts:** `profile/master-profile.md` only. Bracketed fields require Qian's confirmation.

## Core application answers

### Primary role

Senior Data Engineer

### Professional headline

Senior Data Engineer | Pipelines, Migration, and Large-Scale Data Cleaning

### Location and availability

- **Location:** Yokohama, Japan (JST, UTC+9)
- **Citizenship:** Canadian
- **Work model:** Remote
- **Preferred engagements:** Clearly scoped projects lasting approximately two to three months
- **Availability pattern:** Available now, on an ongoing basis; a few substantial projects per year; up to 20 hours per week
- **Regional fit:** Hong Kong and Singapore offer strong business-hours overlap with JST. North America is workable with a defined partial-overlap window and asynchronous delivery.

### Expertise tags

Use the closest platform equivalents for:

- Data Engineering
- Data Pipelines
- Data Migration
- Data Cleaning
- Data Deduplication
- Data Normalization
- Data Quality
- Python
- SQL
- DuckDB
- Large-Scale Data Processing
- AI-Assisted Software Delivery

Do not add cloud platforms, orchestration products, streaming tools, certifications, or frameworks that are not recorded in the master profile.

### Bio

I am a Canadian senior data engineer based in Yokohama, Japan, with nine years of professional experience (Sun Life, three years; Creative Market, two years; Bonfire, one year; and three years with Japan-based employer Pennery Car Japan — name as spoken, spelling to confirm). I specialize in building data pipelines, delivering data migrations, and cleaning, deduplicating, and normalizing large operational datasets. My core tools are Python, SQL, and DuckDB, and I use AI coding agents extensively to accelerate implementation, testing, analysis, and documentation while retaining direct responsibility for architecture and data-quality decisions.

A recent personal project processed 256,279 Canadian government contract records covering 46,639 suppliers and turned them into ranked supplier intelligence. Since January 2026, I have also been delivering data-engineering work under an ongoing contract with a financial institution, alongside a Japan-based engineering role.

I focus on remote projects with a clear scope and measurable outcome, typically lasting two to three months. I am fluent in English and a native Chinese speaker. My Japanese is conversational for daily life and is not offered as a business-delivery language.

### Rate

- **Preferred Braintrust asking rate:** USD 95/hr
- **Acceptable positioning band:** USD 90–100/hr, subject to scope, duration, meeting load, and contracting structure
- **Researched platform context:** Data roles at approximately USD 70–100/hr
- **Do not quote below:** USD 70/hr equivalent without Qian's explicit approval

If the application requires one number, use **USD 95/hr** after Qian confirms the rate.

### Work authorization / contracting note

Canadian citizen based in Japan. Available for remote engagements through Braintrust or another confirmed compliant contracting structure, which may include a Contractor of Record where required. Contracting entity and cross-border tax structuring are being finalized with a tax advisor.

Do not claim local work authorization for a client's jurisdiction unless the platform confirms the specific arrangement.

## AI-interview preparation notes

These are preparation prompts, not scripted claims. Answers should stay within the facts in the master profile.

### Likely topic: Pipeline design

**Talking points**

- Start from the source format, volume, quality problems, and the decision the output must support.
- Separate ingestion, cleaning/normalization, deduplication, validation, and ranked/analytical output.
- Explain how intermediate outputs make errors visible and reruns safer.
- Use the `cadb2b` project as the concrete example: 256,279 contract records and 46,639 suppliers transformed into ranked supplier intelligence.

### Likely topic: Data migration

**Talking points**

- Define source-to-target mapping before implementation.
- Preserve traceability from source records to migrated outputs.
- Reconcile counts and key fields, sample transformed records, and make validation repeatable.
- Plan cutover and rollback around verified checkpoints rather than a single unverified transfer.

### Likely topic: Cleaning, deduplication, and normalization

**Talking points**

- Distinguish exact duplicates from records that represent the same entity with inconsistent names or attributes.
- Normalize formats before matching; otherwise matching rules operate on avoidable noise.
- Keep match logic explainable and review samples from both accepted and rejected matches.
- Measure success by downstream usability, not just by the number of rows removed.

### Likely topic: Python, SQL, and DuckDB

**Talking points**

- Python is appropriate for ingestion, transformation logic, automation, and repeatable processing.
- SQL is the language for inspection, joins, reconciliation, aggregation, and validation.
- DuckDB is effective for analytical processing over large local or file-based datasets.
- Be ready to discuss tradeoffs, query validation, and how to profile a slow or incorrect transformation. Do not claim tools or production environments that are not in the master profile.

### Likely topic: Scale and data quality

**Talking points**

- Use the verified scale points: 256,279 records and 46,639 suppliers.
- Discuss profiling before transformation, explicit quality checks, exception handling, and reproducible reruns.
- Explain how ranked output was validated against the underlying records.

### Likely topic: AI-assisted delivery

**Talking points**

- AI coding agents accelerate implementation, boilerplate, test drafting, exploration, and documentation.
- Human ownership remains with Qian for architecture, source interpretation, matching rules, validation, and final acceptance.
- Review generated code and verify outputs against data; do not present AI assistance as unsupervised delivery.
- Be prepared to explain a case where generated output would need correction after inspection or testing, without inventing a client incident.

### Likely topic: Remote delivery across time zones

**Talking points**

- Yokohama provides strong overlap with Hong Kong and Singapore and partial overlap with North America.
- Use written progress notes, explicit blockers, and scheduled decision windows to reduce dependence on simultaneous working hours.
- Confirm the client's required meeting window before accepting an engagement.

### Likely topic: Communication and stakeholder management

**Talking points**

- English is the professional working language; prior work experience includes Canada.
- Clarify the business decision, required fields, quality thresholds, and acceptance checks at kickoff.
- Report progress in terms of records processed, issues found, validation status, and remaining risks.

## Pre-submission checklist

- [x] Professional display name and contact email confirmed: Ruoyu Qian / ruoyucad@gmail.com
- [x] Years of experience confirmed: 9 years (Sun Life 3, Creative Market 2, Bonfire 1, Japan-based employer 3)
- [x] Weekly capacity confirmed: up to 20 hours per week
- [x] Portfolio approved: anything useful from Qian's GitHub repositories may be used as portfolio material; `cadb2b` is the flagship piece but is a **private** repo — present it as a project description and offer a code walkthrough during screening rather than a public link
- [ ] Qian gives final confirmation of USD 95/hr as the single-number rate
- [ ] Japan employer name spelling confirmed before the Japan role is named (currently written as spoken: "Pennery Car Japan" [employer name spelling to confirm])
- [ ] Qian verifies every expertise tag against actual experience
- [ ] No financial-institution name has been added without approval
- [ ] Japanese is described only as daily-life conversational ability
