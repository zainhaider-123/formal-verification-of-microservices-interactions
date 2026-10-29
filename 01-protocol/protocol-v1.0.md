# Systematic Review Protocol (PRISMA-P 2015 + PRISMA 2020 alignment)

**Title:** From Microservices to Modular Monoliths: A Systematic Review of
Architectural Consolidation Patterns, Motivations, and Outcomes (2020-2026)

**Version:** 1.0
**Date:** 2026-03-23
**Registered at:** OSF Registries (DOI placeholder: 10.17605/OSF.IO/XXXXX)
**Reporting guideline followed:** PRISMA 2020 (Page et al., BMJ 2021;372:n71)

This protocol follows the PRISMA-P 2015 reporting checklist for systematic
review protocols (Moher et al., Syst Rev 2015;4:1).

## 1. Administrative information

### 1.1 Title
See above.

### 1.2 Registration
OSF Registries, DOI to be assigned at registration.

### 1.3 Authors
[Author list with affiliations and contributions]

### 1.4 Amendments
None as of v1.0. Future amendments will be documented in the decision log
with justification, date, and impact on the review.

### 1.5 Support
[Funding source]

## 2. Introduction

### 2.1 Rationale (PRISMA-P item 6a)

Microservices architecture dominated software system design from 2014 through
the early 2020s, promising scalability, organizational autonomy, and
deployment independence. Starting around 2020 and accelerating after several
high-profile industry cases (Amazon Prime Video's 2023 consolidation being
widely cited), organizations began reporting that microservices introduced
operational complexity, latency, and cost overheads that outweighed benefits
for many applications. The term "modular monolith" emerged to describe a
middle-ground architecture retaining modularity benefits without distributed-
system overheads.

Despite substantial industry discussion, no rigorous systematic synthesis of
peer-reviewed empirical studies on this consolidation trend has been
conducted. Existing reviews focus on decomposition (monolith to microservices)
rather than the reverse trajectory.

### 2.2 Objectives (PRISMA-P item 6b)

To systematically synthesize peer-reviewed empirical literature on
microservices-to-modular-monolith consolidation in order to:
1. Identify motivations and drivers for consolidation.
2. Catalog consolidation patterns, decision frameworks, and strategies.
3. Characterize reported outcomes and evaluation approaches.
4. Identify open challenges and research gaps.

## 3. Methods

### 3.1 Eligibility criteria (PRISMA-P item 8 / PRISMA 2020 item 5)

**Inclusion criteria:**
- Peer-reviewed journal articles or peer-reviewed conference papers at
  CORE A* or A venues
- Published between January 2020 and June 2026
- Written in English
- Reports an empirical study (case study, multi-case study, experiment,
  survey, or mining study) on at least one documented instance of
  microservices-to-modular-monolith consolidation
- Provides sufficient detail about motivations, process, or outcomes

**Exclusion criteria:**
- Surveys, reviews, mappings, position papers, opinion pieces
- Industry whitepapers, blog posts, technical reports, theses
- Papers focused on monolith-to-microservices decomposition without
  documenting subsequent consolidation
- Short papers under 4 pages, extended abstracts, posters
- Papers that only compare architectural styles conceptually without
  empirical cases
- Papers with insufficient methodological detail

### 3.2 Information sources (PRISMA-P item 9 / PRISMA 2020 item 6)

Six bibliographic databases will be searched on a single date:

1. ACM Digital Library
2. IEEE Xplore
3. Scopus
4. Web of Science Core Collection
5. ScienceDirect (Elsevier)
6. SpringerLink

### 3.3 Search strategy (PRISMA-P item 10 / PRISMA 2020 item 7)

A canonical Boolean search string was developed iteratively with the
information specialist and pilot-tested. The string targets three concept
blocks combined with AND:

- Block 1: microservices and related decomposition terminology
- Block 2: consolidation, merging, or modular monolith terminology
- Block 3: empirical study terminology (case study, experience, migration,
  refactoring)

The full canonical string is in `02-searches/search-string-canonical.txt`.
Database-specific adaptations are in dated files in the same folder.

The search was peer-reviewed by a second information specialist using the
PRESS 2015 checklist (McGowan et al., J Clin Epidemiol 2016;75:40-46)
before execution. PRESS comments are documented in
`02-searches/press-peer-review.md`.

### 3.4 Study records (PRISMA-P item 11 / PRISMA 2020 item 8)

**Data management:** Records will be exported from each database in BibTeX
or RIS format and imported to Rayyan for deduplication and screening.

**Selection process:** Two reviewers (R1, R2) will independently screen all
records at title/abstract and full-text stages with reviewer blinding
enabled. Cohen's kappa will be calculated for both stages. Disagreements
will be resolved through discussion; unresolved disagreements adjudicated
by the guarantor.

**Data collection process:** Two reviewers will independently extract data
from all included studies into a shared structured form.

### 3.5 Data items (PRISMA-P item 12 / PRISMA 2020 item 10)

The data extraction form captures: bibliographic data, study design, system
characteristics (domain, team size, codebase size, number of microservices
before/after), consolidation motivations, consolidation strategy, tooling
used, reported outcomes (quality attributes, cost, productivity), and
limitations.

### 3.6 Outcomes and prioritization (PRISMA-P item 13 / PRISMA 2020 item 9)

Primary outcomes:
- Reported motivations/drivers for consolidation (RQ1)
- Reported strategies and patterns (RQ2)
- Reported post-consolidation outcomes (RQ3)

Secondary outcomes:
- Tooling and automation used
- Team and organizational structure changes
- Time and effort required

### 3.7 Risk of bias (PRISMA-P item 14 / PRISMA 2020 item 11)

A custom risk of bias assessment instrument adapted for empirical software
engineering case studies will be applied to each included study by two
independent reviewers. The instrument is described in
`06-risk-of-bias/rob-instrument.md`.

### 3.8 Data synthesis (PRISMA-P item 15 / PRISMA 2020 item 13)

Narrative synthesis is planned. Quantitative synthesis (meta-analysis) is
**not** planned because primary studies use heterogeneous system sizes,
measurement approaches, and outcome definitions, making numerical pooling
inappropriate.

Synthesis will be organized by research question with thematic coding for
qualitative data on motivations and challenges.

### 3.9 Meta-bias and certainty (PRISMA 2020 items 14, 15)

Reporting bias will be assessed by examining whether studies report
negative results (failed consolidations), by checking alignment between
stated research questions and reported outcomes, and by looking for
publication patterns suggesting positive-result bias.

Certainty in the synthesis will be discussed narratively, considering
risk of bias, consistency, directness, and precision of evidence across
included studies.

## 4. Reporting

The completed review will be reported strictly per PRISMA 2020 with the
27-item checklist completed and a PRISMA 2020 flow diagram included.
Target venue: Empirical Software Engineering (Springer) or IEEE Software.

## 5. Replication package

A replication package containing search strings, screening logs, extraction
data, risk of bias assessments, and the completed PRISMA checklist will be
deposited on Zenodo with a DOI before manuscript submission.
