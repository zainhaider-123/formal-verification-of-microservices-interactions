# Systematic Review Protocol (PRISMA-P 2015 + PRISMA 2020 alignment)

**Title:** Formal Verification of Microservice Interactions

**Version:** 1.1
**Date:** 2026-11-07
**Authors:** Zain Haider, Ashok Kumar (NED University)
**Registration:** Not registered (coursework); protocol decisions and amendments will be recorded in `00-admin/decision-log.md`
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

Version 1.1 clarifies the research questions, microservice-interaction scope, eligibility rules, screening decisions, extraction fields, and synthesis procedures. These are protocol decisions, not completed review findings. This revision and subsequent amendments will be recorded in the decision log with their date, justification, review stage, and impact. Eligibility changes made after screening begins will trigger reassessment of affected records.

### 1.5 Support
None (coursework).

## 2. Introduction

### 2.1 Rationale (PRISMA-P item 6a)

Microservice systems depend on communication and coordination among independently deployable services. This review focuses on correctness of interactions such as request–response communication, asynchronous messaging, event-driven coordination, orchestration, choreography, and distributed workflows or transactions. Relevant failures include incompatible protocols, incorrect message ordering, deadlock, failure to complete workflows, and violations of cross-service consistency requirements.

Formal verification establishes whether explicitly specified properties hold under stated models and assumptions. The review will examine how interactions are represented, which properties are verified, how verification is performed, and what limits the approaches. Guarantees for a formal model will be distinguished from claims about executable services, recording any evidence connecting the two. Verification of isolated internal service logic is outside scope unless the verified property explicitly concerns interaction with another microservice.

### 2.2 Objectives (PRISMA-P item 6b)

To systematically identify, classify, and synthesize primary studies on formal verification of microservice interactions using four research questions:
1. **RQ1. Which formal modelling approaches are used to represent microservice interactions, and what aspects of these interactions do they capture?** Identify formalisms, communication semantics, coordination patterns, and assumptions.
2. **RQ2. Which correctness properties of microservice interactions are formally specified and verified?** Identify property categories, formal expressions, outcomes, and guarantee scope.
3. **RQ3. Which formal verification techniques and tools are used to verify these properties, and how are they applied?** Identify verification procedures, tool support, automation, and links between specifications, models, and implementations.
4. **RQ4. What scalability challenges and other limitations are reported for the formal verification of microservice interactions?** Identify measured scaling behaviour, reported obstacles, restrictive assumptions, and supporting evidence.

## 3. Methods

### 3.1 Eligibility criteria (PRISMA-P item 8 / PRISMA 2020 item 5)

**Inclusion criteria:**
- **IC1 — Publication type:** Peer-reviewed primary research in a journal or conference proceedings, reporting an original method, tool, formal result, or application. Workshop papers qualify only when peer reviewed, published in conference proceedings, and meeting all other criteria.
- **IC2 — Publication period:** First formal publication of the report, including an online-first journal version, falls between 1 January 2018 and the final search date in 2026. Record the actual cutoff; later 2026 publications qualify only if available by that date. The 2018 lower bound retains the coursework scope and limits conclusions about earlier research.
- **IC3 — Language and length:** Full text in English with at least four pages of main article content, excluding reference-only pages and supplementary material.
- **IC4 — Microservice context:** Explicitly studies microservices or concretely applies its method to a microservice system. Generic service-oriented/distributed methods qualify only with a worked microservice application and interaction-verification results. Incidental mentions or potential applicability are insufficient.
- **IC5 — Interaction focus:** The verified property concerns communication, coordination, compatibility, composition, or shared behaviour across at least two microservices, or between a microservice and an explicitly modelled microservice peer. Composed models and abstract environments qualify when service roles and communication behaviour are identifiable.
- **IC6 — Formal verification:** Uses a mathematically defined representation or semantics, identifies an interaction property, and reports a formal verification procedure and outcome. Outcomes may include proofs, satisfied/violated properties, counterexamples, inconclusive results, or timeouts. Manual proofs qualify; automated tools are not mandatory.
- **IC7 — Assessable detail:** The accessible full text identifies the interaction, model or formal semantics, target property, verification procedure, and outcome sufficiently for extraction. Industrial deployment, public artifacts, scalability experiments, and answers to every RQ are not required.

**Exclusion criteria:**
- **EC1:** Surveys, reviews, mappings, and position/opinion papers without an eligible original verification contribution. Secondary studies may support background and citation searching but will not enter the primary-study synthesis.
- **EC2:** Non-peer-reviewed publications, including unpublished preprints, whitepapers, blogs, technical reports, and theses; also extended abstracts, posters, tutorials, and publication types failing IC1.
- **EC3:** Reports outside the date window, non-English full texts, or reports below the minimum main-text length.
- **EC4:** Generic web-service, service-oriented, cloud, or distributed-system studies lacking the concrete microservice application required by IC4.
- **EC5:** Internal single-service correctness, infrastructure, deployment, resource allocation, or other analyses without a verified interaction property. Security, timing, reliability, and consistency studies remain eligible when their verified properties concern microservice interactions.
- **EC6:** Informal/semi-formal modelling without formal verification results; testing, simulation, tracing, or monitoring alone. Runtime verification qualifies only when formally specified interaction properties are checked using defined verification semantics. Model-based testing alone does not qualify.
- **EC7:** Missing essential technical elements in IC7 after full-text assessment. Missing tool versions, artifacts, benchmarks, or scalability measurements alone will be recorded as reporting limitations rather than exclusions.

All inclusion criteria must be met. Naming a formalism alone does not establish eligibility. Uncertain title/abstract records will proceed to full text. Duplicate records will be removed before screening. Related reports of one underlying study will be linked: the most complete report supplies the main evidence, with unique information retained from companions. Unretrievable reports will be recorded separately from assessed full-text exclusions.

### 3.2 Information sources (PRISMA-P item 9 / PRISMA 2020 item 6)

Six bibliographic databases will be searched:

1. ACM Digital Library
2. IEEE Xplore
3. Scopus
4. Web of Science Core Collection
5. ScienceDirect (Elsevier)
6. SpringerLink

For each source, record platform, coverage, exact query, fields, filters, date, result count, and export file. Document access limitations or substitutions. One round of backward reference checking and forward citation searching of included studies will supplement database searches; relevant reviews may also supply candidates. Supplementary records must meet the same criteria and be deduplicated, with discovery source/date recorded. Document any additional citation-searching rounds.

### 3.3 Search strategy (PRISMA-P item 10 / PRISMA 2020 item 7)

A canonical Boolean search string will be developed iteratively and pilot-tested. The string targets three concept blocks combined with AND:

- Block 1: microservices terminology, initially `microservice* OR "micro-service*" OR "micro service*"`.
- Block 2: formal verification / formal methods terminology, initially `"formal verif*" OR "formal method*" OR "model check*" OR "theorem prov*" OR "Petri net*" OR "process calcul*" OR "session type*" OR "behavioural type*" OR "behavioral type*" OR "temporal logic" OR "runtime verif*" OR SMT`.
- Block 3: interaction / communication terminology, initially `interact* OR communicat* OR coordinat* OR compos* OR choreograph* OR orchestrat* OR protocol* OR messag* OR workflow* OR transaction* OR deadlock*`.

These are initial search terms, not eligibility requirements or findings. Search titles, abstracts, and keywords where supported. Adapt fields, wildcards, and phrase syntax to each platform and pilot against a documented set of known relevant papers identified during scoping. A supplementary search using Blocks 1 AND 2 will reduce dependence on explicit interaction terminology; its results will also be logged and deduplicated. Date and language filters will be used where reliable; other criteria will be applied during screening.

The full canonical string will be stored in `02-searches/search-string-canonical.txt`, with database-specific adaptations, pilot changes, and dated logs in the same folder. Definitive queries will be fixed before main searching. Updates before submission will use the recorded strategy and be reported separately.

### 3.4 Study records (PRISMA-P item 11 / PRISMA 2020 item 8)

**Data management:** Export records in BibTeX or RIS format and preserve raw exports. Deduplicate using DOI matching followed by normalized titles, authors, and years, manually resolving uncertain matches. Stable record, report, and study identifiers will connect searches, screening, full texts, and extraction. Related reports will be linked without double-counting shared evidence.

**Selection process:** Two reviewers (Zain Haider, Ashok Kumar) will independently screen all records at title/abstract and full-text stages. Pilot the criteria on 30 records and five full texts, or all available records/reports if fewer, and reconcile interpretations before full screening. Retain uncertain title/abstract cases. At full text, record eligibility evidence and one primary exclusion reason, using the first applicable EC code in the order above. Resolve disagreements through discussion and document the resolution; unresolved cases remain pending until consensus. Log retrieval attempts and reports not retrieved. Counts will support the PRISMA flow diagram.

**Data collection process:** Two reviewers will independently extract all included studies into a shared form, piloted on three studies or all studies if fewer. Substantive entries will include page, section, table, or artifact references. Resolve discrepancies against the source. Mark missing data “not reported”; use “not applicable” only with justification. Separate author statements from reviewer interpretations. Data collection corresponds to PRISMA 2020 item 9.

### 3.5 Data items (PRISMA-P item 12 / PRISMA 2020 item 10)

The extraction form captures bibliographic data, linked study/report identifiers, contribution type, domain, and evaluation setting, together with:

- **RQ1:** Formalism and role; service roles; synchronous/asynchronous communication; interaction patterns; ordering, delivery, queue bounds, and failure assumptions; dynamic behaviour; and manual/automated model construction.
- **RQ2:** Property name, normalized category, formal specification or proof obligation, local/cross-service scope, outcome, and guarantee conditions. Categories may include safety, liveness, deadlock freedom, compatibility, consistency, timing, and security; retain original author terminology alongside review categories.
- **RQ3:** Technique, tool/version when reported, tool role, inputs, automation, abstraction/compositional/reduction mechanisms, boundedness, and correspondence between verified models and executable services. Code modelling formalisms, property languages, verification techniques, and tools separately.
- **RQ4:** Service counts, states/transitions, queue bounds, workloads, and other scale parameters; runtime, memory, hardware, timeouts, and resource limits when reported; factors varied; bottlenecks; mitigation; residual restrictions; and applicability threats. Distinguish measured results, author-discussed limitations, and reviewer inferences.

Evaluation settings will distinguish illustrative examples, synthetic benchmarks, open-source applications, and industrial cases. “Scalability not evaluated” will not be interpreted as evidence of scalability. Extract failed and inconclusive verification outcomes alongside successful outcomes.

### 3.6 Outcomes and prioritization (PRISMA-P item 13 / PRISMA 2020 item 9)

Primary outcomes (mapped to research questions):
- Formal modelling approaches and captured interaction aspects (RQ1).
- Formally specified and verified properties, outcomes, and guarantee scope (RQ2).
- Verification techniques, tools, and application workflows (RQ3).
- Reported scalability challenges and other limitations, with evidence and conditions (RQ4).

All four outcomes have equal priority. Evaluation setting, reproducibility, and evidence quality will contextualize findings. Frequency of use will not establish superiority. Outcome definitions correspond to PRISMA 2020 item 10a; item 9 concerns data collection and is addressed in Section 3.4. Original heading labels have been retained.

### 3.7 Risk of bias (PRISMA-P item 14 / PRISMA 2020 item 11)

Two independent reviewers will assess each study using a review-specific technical quality/risk-of-bias instrument, described in `06-risk-of-bias/rob-instrument.md` and piloted before full use. This is not a validated clinical risk-of-bias instrument.

Domains will cover clarity of interaction models and assumptions; precise property definitions; transparency of verification procedures and outcomes; justification of correctness claims; adequacy of evaluation for the claims made; reproducibility; and treatment of limitations. Rate each domain “adequate,” “partly adequate,” “inadequate,” or “not applicable,” with source-based justification. Resolve disagreements through discussion. No aggregate score cutoff will exclude otherwise eligible studies. Domain concerns will qualify synthesis claims. Studies making no scalability claims will not be penalized solely for lacking scaling experiments.

### 3.8 Data synthesis (PRISMA-P item 15 / PRISMA 2020 item 13)

Narrative synthesis will be organized by RQ1–RQ4, supported by descriptive tables and thematic coding. An extraction-based codebook will be refined during piloting; changes will be logged and applied to earlier extractions. Multiple categories may apply to a study. Counts and percentages will state denominators and use underlying studies, rather than duplicate reports, as the main counting unit.

RQ1 will map formalisms to captured interaction semantics. RQ2 will map properties to interaction patterns and outcomes. RQ3 will relate techniques/tools to supported models and properties. RQ4 will distinguish experimentally observed scaling behaviour, stated restrictions, and evidence gaps. Cross-tabulations will connect findings where data permit.

Runtime and memory results will retain model size, bounds, hardware, and settings where available. Incompatible experimental settings will not be pooled or used to rank tools. Meta-analysis is not planned because verification tasks and evaluation conditions are expected to differ. Examine patterns by evaluation setting and methodological concerns; identify conclusions dependent on studies with substantial quality concerns. Unreported limitations will not be interpreted as absent limitations.

### 3.9 Meta-bias and certainty (PRISMA 2020 items 14, 15)

Potential reporting bias will be considered by comparing stated objectives and property claims with reported outcomes, noting missing results/settings and disclosure of negative or inconclusive results. Absence of negative results alone will not demonstrate bias. Related reports may reveal selective presentation. Peer-reviewed-only, language, date, database coverage, and full-text availability restrictions will be discussed as possible sources of incomplete evidence. Funnel plots and publication-bias tests are not planned because there is no common effect estimate.

Confidence in each synthesis finding will be discussed narratively using methodological quality, direct relevance, consistency, evaluation settings, and evidence completeness. Conflicts, reliance on small bounded examples, and absent scalability data will be explicit. This is a review-specific qualitative judgment, not a formal GRADE assessment or evidence of unrestricted correctness of deployed systems.

## 4. Reporting

The completed coursework review will use the PRISMA 2020 27-item checklist and flow diagram, marking inapplicable items with reasons and explaining software engineering adaptations. It will report search dates/queries, identification and deduplication counts, screening/retrieval outcomes, full-text exclusions and reasons, included studies and related reports, quality assessments, and RQ1–RQ4 findings. Amendments, review limitations, support, competing interests, and material availability will be disclosed. PRISMA guidelines support reporting; they do not replace the review-specific methods defined here. Official checklists: [PRISMA-P](https://www.prisma-statement.org/protocols) and [PRISMA 2020](https://www.prisma-statement.org/prisma-2020-checklist).

## 5. Replication package

A replication package will be compiled in `09-supplementary/`, containing the versioned protocol/decision log, exact searches and dates, exports where redistribution is permitted, deduplication rules, screening decisions and exclusion reasons, linked study/report identifiers, extraction form/codebook, extracted evidence, quality assessments, synthesis tables/scripts, completed PRISMA checklist, and flow diagram. A README will explain the files and reproduction of counts. Copyrighted full texts will be replaced by identifiers and source links unless redistribution is permitted.


