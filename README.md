# Systematic Review (Pure PRISMA 2020 Template)

**Topic:** From Microservices to Modular Monoliths: A Systematic Review of
Architectural Consolidation Patterns, Motivations, and Outcomes (2020-2026)

**Methodology:** PRISMA 2020 — Preferred Reporting Items for Systematic
Reviews and Meta-Analyses (Page et al., BMJ 2021;372:n71)

## About this template

This is a sample template demonstrating folder structure and spreadsheet
organization for a systematic review conducted **strictly under PRISMA 2020**.
It does not incorporate Kitchenham & Charters software engineering
methodology, Wohlin snowballing procedures, or other community extensions.

## Topic relevance

The consolidation of microservices back into modular monoliths is one of
the most actively debated topics in advanced software system architecture
research as of 2025-2026. Major indicators:

- **ICSE 2025 SATrends Workshop** dedicated sessions to post-monolith
  architecture and strategic microservices consolidation
- **CNCF Annual Survey (2025)** found ~42% of organizations that adopted
  microservices are consolidating some services into modular monoliths
- **Industry reports** (O'Reilly Technology Trends, Gartner) document a
  ~24% decline in microservices content consumption in 2025
- Key venues: ICSE, ICSA, FSE, ESEC/FSE, Empirical Software Engineering,
  IEEE Software, Journal of Systems and Software, Information and
  Software Technology

### Disclaimer

All numbers, papers, authors, and DOIs in this template are illustrative.
Do not cite anything from this template in real academic work.

## How to use this template

1. Copy this entire folder to start your own systematic review.
2. Rename the top-level folder to reflect your topic.
3. Replace topic-specific content in `01-protocol/` with your own research
   questions and PICO/PECO/PCC.
4. Empty the example data in screening and extraction spreadsheets while
   keeping the column structure.
5. Update `00-admin/` for your team and timeline.
6. Register your protocol on OSF Registries before beginning data collection.

## Folder layout

```
SLR-Modular-Monolith-Consolidation/
|-- 00-admin/                   Team, timeline, decision log
|-- 01-protocol/                Registered protocol with PRISMA-P alignment
|-- 02-searches/                Database search strings and exports
|-- 03-screening/               Title/abstract and full-text screening
|-- 04-included-studies/        Master list and PDFs
|-- 05-data-extraction/         Extraction form and populated sheet
|-- 06-risk-of-bias/            Risk of bias assessment per PRISMA item 11
|-- 07-synthesis/               Narrative synthesis and analysis
|-- 08-manuscript/              Drafts, PRISMA flow diagram, checklist
|-- 09-supplementary/           Replication materials for reviewers
\-- 10-prisma-checklist/        Item-by-item PRISMA 2020 compliance
```

## PRISMA 2020 reference

Page MJ, McKenzie JE, Bossuyt PM, et al. The PRISMA 2020 statement: an
updated guideline for reporting systematic reviews. BMJ 2021;372:n71.
doi:10.1136/bmj.n71
