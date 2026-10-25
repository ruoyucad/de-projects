# Toptal Application Draft

**Status:** Ready-to-review draft; not yet submitted.  
**Source of facts:** `profile/master-profile.md` only. Stage names and requirements must be checked in Toptal's live application flow at submission time.

## Application positioning

### Role

Senior Data Engineer

### Headline

Senior Data Engineer | Pipelines, Migration, and Large-Scale Data Cleaning

### Short positioning statement

Canadian senior data engineer based in Yokohama, Japan, with nine years of professional experience (Sun Life, three years; Creative Market, two years; Bonfire, one year; and three years with a Japan-based employer), focused on remote, clearly scoped data-engineering projects. Core strengths are data pipelines, data migration, and large-scale cleaning, deduplication, and normalization using Python, SQL, and DuckDB. A personal portfolio project processed 256,279 Canadian government contract records covering 46,639 suppliers into ranked supplier intelligence. Since January 2026, also engaged in ongoing data-engineering work for a financial institution under a USD 6,600/month contract, alongside the Japan-based engineering role.

### Target engagement

- **Duration:** Two to three months preferred
- **Volume:** A few substantial projects per year
- **Regions:** North America remote; Hong Kong and Singapore remote
- **Timezone:** JST (UTC+9), with strong APAC overlap and defined partial overlap for North America
- **Weekly capacity:** Up to 20 hours per week
- **Target Toptal rate:** USD 110–130/hr, subject to Qian's final confirmation and Toptal's process

## Screening stages checklist

Use this as a preparation checklist. Confirm the current order and labels inside Toptal when applying.

- [ ] **Initial application**
  - [x] Professional display name and contact details confirmed: Ruoyu Qian / ruoyucad@gmail.com
  - [ ] Senior Data Engineer selected as the primary role
  - [ ] Location entered as Yokohama, Japan
  - [ ] Canadian citizenship and remote-work model stated accurately
  - [ ] Rate expectation prepared: USD 110–130/hr target band (final rate confirmation still open)
  - [ ] Availability pattern stated as project-based, typically two to three months, up to 20 hours per week

- [ ] **English and communication interview**
  - [ ] Prepare a two-minute spoken introduction
  - [ ] Prepare concise explanations of the `cadb2b` project, the ongoing contract work, and the desired engagement pattern
  - [ ] Be ready to explain decisions, tradeoffs, blockers, and validation in clear English
  - [ ] Do not overstate Japanese; it is daily-life conversational only

- [ ] **Technical / algorithm screening**
  - [ ] Review Python problem-solving and clean implementation
  - [ ] Review SQL joins, aggregation, filtering, window logic, and reconciliation queries
  - [ ] Review data structures, complexity, edge cases, and testing approach
  - [ ] Practice explaining reasoning aloud while coding

- [ ] **Technical deep dive / experience review**
  - [ ] Walk through pipeline architecture and data-quality decisions using `cadb2b`
  - [ ] Explain deduplication and normalization choices without inventing tools or infrastructure
  - [ ] Distinguish personal-project facts from confidential contract work
  - [ ] Do not name the financial institution or disclose non-public details

- [ ] **Screening project**
  - [ ] Confirm scope, deadline, evaluation criteria, and permitted AI/tool use before starting
  - [ ] Build a clean repository with a clear README and reproducible setup
  - [ ] Include validation and tests proportionate to the brief
  - [ ] Present the solution, tradeoffs, limitations, and next steps clearly

- [ ] **Professional presentation / final review**
  - [ ] Portfolio project description below is approved by Qian
  - [ ] Public links are supplied only if Qian wants them visible
  - [ ] Availability, timezone overlap, and contracting constraints are stated without ambiguity

## Portfolio project to submit: `cadb2b`

### Project title

**Canadian Government Contract Intelligence Pipeline (`cadb2b`)**

### Project description

`cadb2b` is a personal data-engineering project that transforms a large collection of Canadian government contract records into ranked supplier intelligence.

The pipeline processed **256,279 contract records** covering **46,639 suppliers**. The work required handling a dataset large enough that manual inspection could not establish reliable supplier-level conclusions. Source records had to be organized, cleaned, normalized, and deduplicated so contracts could be analyzed consistently at supplier level and converted into a ranked intelligence output.

The project demonstrates the core work Qian offers to clients:

- Designing a repeatable pipeline for a large, messy dataset
- Cleaning and standardizing records before analysis
- Normalizing supplier information across a large supplier population
- Deduplicating and reconciling records so downstream rankings are defensible
- Using Python, SQL, and DuckDB to inspect, transform, validate, and rank data
- Turning raw administrative records into a structured output that supports commercial decisions

### Portfolio summary (short version)

Built a Python, SQL, and DuckDB pipeline that processed 256,279 Canadian government contract records across 46,639 suppliers. Cleaned, normalized, and deduplicated the dataset and produced ranked supplier intelligence, demonstrating large-scale data processing, data-quality controls, and analytical dataset design.

### What to emphasize in the screening conversation

- The scale is concrete and verifiable from the project outputs: 256,279 records and 46,639 suppliers.
- The difficult part is not simply loading data; it is making inconsistent records comparable enough to support ranking.
- Validation matters at each stage: source counts, transformed counts, supplier-level aggregation, and sample inspection.
- AI coding agents can accelerate implementation and documentation, but architecture, matching rules, and quality decisions remain human-owned.

### What not to claim

- Do not claim a client, employer, production users, revenue, or commercial deployment for `cadb2b` unless Qian adds that fact to the master profile.
- Do not add cloud services, orchestration tools, databases, or frameworks that are not documented in the project materials Qian approves for screening.
- Do not identify the separate financial-institution client or use its work as a public case study.

### Portfolio link

- GitHub: https://github.com/ruoyucad/cadb2b
- Visibility: Qian has approved linking his GitHub repositories in applications and describing/showcasing them during screening.

## English and communication notes

- English is Qian's professional working language and is fluent; he has worked in Canada.
- Prepare answers in a consistent structure: context, problem, approach, validation, result, limitation.
- Keep the introduction selective: senior data engineering, large-scale messy data, project-based remote delivery, and JST positioning.
- For North American clients, state the proposed overlap window explicitly rather than implying full local-hours coverage.
- For Hong Kong and Singapore, emphasize the practical advantage of being one hour ahead of those markets.
- Japanese should be mentioned only if asked: conversational for daily life, not a business-delivery language.

## Test-project readiness checklist

- [ ] Development environment can run Python, SQL-based analysis, and DuckDB from a clean checkout
- [ ] Git workflow and repository hygiene reviewed
- [ ] README structure prepared: problem, setup, run steps, architecture, validation, tradeoffs, limitations
- [ ] Testing approach prepared for transformations, edge cases, and reconciliation checks
- [ ] Time blocked for the full screening-project window
- [ ] Current Toptal rules on AI assistance checked before using any AI coding agent
- [ ] No confidential material from the financial-institution contract is reused
- [ ] Demo data and repository contain no passport, tax, banking, or other sensitive personal documents
- [ ] Presentation rehearsed: five-minute walkthrough and fifteen-minute deep dive
- [ ] Questions prepared on scope, acceptance criteria, data access, review cadence, and decision ownership

## Pre-submission inputs still required from Qian

- Japan employer name spelling, before the Japan role is named: [Japan employer name — to confirm spelling]
- Approved CV/resume
- Final Toptal rate confirmation within or outside the USD 110–130/hr target band
- Confirmed start window (weekly capacity is confirmed: up to 20 hours per week)
- Confirmation of contracting route and tax-structuring status with his advisor

Already confirmed: 9 years of experience with employer history (Sun Life 3 years, Creative Market 2 years, Bonfire 1 year, Japan-based employer 3 years); display name Ruoyu Qian and email ruoyucad@gmail.com; `cadb2b` GitHub link approved for applications and screening.
