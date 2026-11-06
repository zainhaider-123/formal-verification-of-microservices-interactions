# Systematic Review Protocol (PRISMA-P 2015 + PRISMA 2020 alignment)

**Title:** Formal Verification of Microservice Interactions

**Version:** 1.0
**Date:** 2026-10-29
**Authors:** Zain Haider, Ashok Kumar (NED University)
**Registration:** Not required for coursework; protocol followed as documented here and in `00-admin/decision-log.md`
**Reporting guideline followed:** PRISMA 2020 (Page et al., BMJ 2021;372:n71)

This protocol follows the PRISMA-P 2015 reporting checklist for systematic
review protocols (Moher et al., Syst Rev 2015;4:1).

## 1. Administrative information

### 1.1 Title
Formal Verification of Microservice Interactions

### 1.2 Registration
Not applicable (coursework assignment).

### 1.3 Authors
- Zain Haider — NED University
- Ashok Kumar — NED University

### 1.4 Amendments
None as of v1.0. Future amendments will be documented in the decision log
with justification, date, and impact on the review.

### 1.5 Support
None (coursework).

## 2. Introduction

### 2.1 Rationale (PRISMA-P item 6a)

Microservice-based systems coordinate functionality through interactions
between independently developed and deployed services. Errors in these
interactions (e.g., protocol violations, ordering violations, deadlock) can
be difficult to detect by testing alone. Formal verification offers
mathematically grounded techniques for checking whether specified properties
hold of system models. A range of formal modelling approaches, properties,
techniques, and tools have been proposed in the literature for microservice
interactions. This review aims to systematically map and synthesize that
literature so that the state of the art, what has been verified, and the
reported scalability limits are clearly characterized.

### 2.2 Objectives (PRISMA-P item 6b)

To systematically synthesize the literature on formal verification of
microservice interactions in order to:
1. Identify the formal modelling approaches used to represent interactions
   between microservices (RQ1).
2. Identify which properties of microservice interactions are formally
   verified (RQ2).
3. Identify the formal verification techniques and tools used (RQ3).
4. Identify reported scalability problems and limitations (RQ4).

## 3. Methods

### 3.1 Eligibility criteria (PRISMA-P item 8 / PRISMA 2020 item 5)

**Inclusion criteria:**
- Peer-reviewed journal articles or peer-reviewed conference papers
- Published between 2018 and 2026
- Written in English
- Focuses on formal modelling and/or formal verification of interactions
  between microservices (or closely related service-based systems where
  microservice interactions are the object of verification)
- Provides sufficient detail about at least one of: modelling approach,
  verified properties, verification technique/tool, or scalability
  limitations

**Exclusion criteria:**
- Surveys, reviews, mappings, position papers, opinion pieces
- Industry whitepapers, blog posts, technical reports, theses
- Papers that do not address formal verification of service/microservice
  interactions (e.g., purely informal testing, or verification of
  non-interaction concerns with no interaction focus)
- Short papers under 4 pages, extended abstracts, posters
- Papers with insufficient methodological or technical detail

### 3.2 Information sources (PRISMA-P item 9 / PRISMA 2020 item 6)

Six bibliographic databases will be searched:

1. ACM Digital Library
2. IEEE Xplore
3. Scopus
4. ScienceDirect (Elsevier)
5. SpringerLink

### 3.3 Search strategy (PRISMA-P item 10 / PRISMA 2020 item 7)

A canonical Boolean search string will be developed iteratively and
pilot-tested. The string targets three concept blocks combined with AND:

- Block 1: microservices terminology
- Block 2: formal verification / formal methods terminology
- Block 3: interaction / communication terminology

The full canonical string will be stored in
`02-searches/search-string-canonical.txt`, with database-specific
adaptations in dated files in the same folder.

### 3.4 Study records (PRISMA-P item 11 / PRISMA 2020 item 8)

**Data management:** Records will be exported from each database in BibTeX
or RIS format and deduplicated.

**Selection process:** Two reviewers (Zain Haider, Ashok Kumar) will
independently screen all records at title/abstract and full-text stages.
Disagreements will be resolved through discussion.

**Data collection process:** Two reviewers will independently extract data
from all included studies into a shared structured form.

### 3.5 Data items (PRISMA-P item 12 / PRISMA 2020 item 10)

The data extraction form captures: bibliographic data, study design/type,
formal modelling approach used (RQ1), properties formally verified (RQ2),
verification techniques and tools used (RQ3), and scalability problems and
limitations reported (RQ4).

### 3.6 Outcomes and prioritization (PRISMA-P item 13 / PRISMA 2020 item 9)

Primary outcomes (mapped to research questions):
- Formal modelling approaches identified (RQ1)
- Properties formally verified identified (RQ2)
- Verification techniques and tools identified (RQ3)
- Scalability problems and limitations identified (RQ4)

### 3.7 Risk of bias (PRISMA-P item 14 / PRISMA 2020 item 11)

A quality/risk-of-bias assessment will be applied to each included study by
two independent reviewers. The instrument will be described in
`06-risk-of-bias/rob-instrument.md`.

### 3.8 Data synthesis (PRISMA-P item 15 / PRISMA 2020 item 13)

Narrative synthesis is planned, organized by research question (RQ1–RQ4),
with thematic coding for qualitative data on modelling approaches,
properties, techniques/tools, and limitations. Quantitative synthesis
(meta-analysis) is not planned because the literature is expected to be
heterogeneous in modelling formalism, system scale, and evaluation approach.

### 3.9 Meta-bias and certainty (PRISMA 2020 items 14, 15)

Reporting bias will be assessed by examining whether studies report negative
or null results and limitations, and by checking alignment between stated
aims and reported outcomes. Certainty in the synthesis will be discussed
narratively, considering quality of included studies, consistency,
directness, and precision of evidence.

## 4. Reporting

The completed review will be reported per PRISMA 2020 with the 27-item
checklist completed and a PRISMA 2020 flow diagram included. This review is
prepared as a coursework assignment.

## 5. Replication package

A replication package containing search strings, screening logs, extraction
data, risk-of-bias assessments, and the completed PRISMA checklist will be
compiled in `09-supplementary/`.
