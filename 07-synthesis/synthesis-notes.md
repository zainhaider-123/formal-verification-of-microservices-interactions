# Synthesis Notes

Working drafts of the narrative synthesis for each research question, to be
refined into the Results section of the manuscript.

## RQ1: Motivations and drivers for consolidation

Thematic coding of the 23 included studies reveals five dominant drivers
that cluster into technical, economic, and organizational categories.

### Technical drivers

**Operational complexity burden (17 studies)** is the most frequently cited
driver. Teams describe the overhead of debugging across service boundaries,
coordinating deployments, managing service meshes, and handling on-call
rotations for many small services. Example from S001 (Fowler et al.): the
team reduced 3am on-call pages from weekly to once every two months after
consolidation.

**Latency in synchronous chains (8 studies)** emerges as a specific technical
driver in request-response heavy applications. S003 (Laurent et al.) reports
p99 latency reduced by 74% after consolidation because in-process calls
replaced network hops.

### Economic drivers

**Cloud infrastructure cost (15 studies)** is the second most frequent
driver. Studies report cost reductions from 34% (S009, mean across 11
companies) to 62% (S003) post-consolidation. The cost reduction comes
primarily from reduced compute overhead, simpler observability, and
elimination of platform engineering roles.

### Organizational drivers

**Team size mismatch (11 studies)** appears when engineering teams are too
small to sustain distributed operations. S001 and S003 both describe teams
under 25 engineers that had adopted microservices following industry trend
advice, only to find the operational burden unsustainable. S007 (Lindqvist
& Petersen) shows the opposite pressure: Conway's Law drove decomposition
as the team grew, then consolidation as it shrank.

**Regulatory/compliance drivers (4 studies)** — rare but distinctive. S005
(Takahashi & Yamada) describes financial regulators requiring unified
transaction boundaries that were technically impossible in distributed
microservices.

## RQ2: Consolidation strategies and patterns

Five distinct strategic patterns emerge from the included studies:

1. **Strangler-fig inversion (9 studies)** — The reverse of the classic
   strangler-fig pattern: instead of extracting services from a monolith,
   teams incrementally absorb microservices back. Examples: S001, S005, S023.
   Typically takes 6-12 months.

2. **Selective consolidation (7 studies)** — Hybrid approach where some
   services are consolidated and others retained. S004 (Hansen & Rasmussen)
   consolidated 25 of 28 services, keeping 3 with distinct scaling profiles.
   S018 (Tanaka & Yoshida) proposes a latency-profile-driven selection.

3. **DDD bounded-context alignment (6 studies)** — Use Domain-Driven Design
   to identify appropriate module boundaries in the target monolith. S008
   (Anand & Yusuf) and S013 (Ramirez & Choi) both emphasize that this
   strategy requires DDD expertise on the team, without which module
   boundaries devolve to arbitrary technical splits.

4. **Big-bang rewrite (2 studies)** — Parallel rewrite with feature parity
   followed by switchover. Only S003 reports success; the authors
   explicitly caution that this strategy is rarely advisable.

5. **Framework-guided (1 study)** — S006 (Morales & Dlamini) proposes a
   decision framework with validation on three cases, but acknowledges
   framework limited to greenfield post-migration scenarios.

### Tooling used

- **ArchUnit** for enforcing module boundaries after consolidation (S001, S008, S013)
- **Spring Modulith** for Java/Spring applications (S001, S008, S012, S017)
- **Feature flags** for controlling migration rollout (S001, S004, S023)
- **Traffic shadowing (Istio)** for validating consolidated services (S004)
- **Structure101** for architecture visualization (S008)

## RQ3: Outcomes and measurement

### Positive outcomes (by frequency)

| Outcome | Studies reporting | Median improvement |
|---|---|---|
| Cloud cost reduction | 14 | ~45% |
| Deployment frequency increase | 6 | ~2x |
| Developer satisfaction | 10 | +25-40% |
| MTTR reduction | 8 | ~60% |
| p99 latency reduction | 5 | ~55% |

### Reported regressions (trade-offs)

| Regression | Studies reporting |
|---|---|
| Loss of failure isolation | 8 |
| Peak-load scalability ceiling | 5 |
| Higher deployment risk per release | 4 |
| Initial DDD/architecture learning curve | 3 |

### Measurement approaches

- **Pre/post operational metrics** (8 studies)
- **Cost/invoice analysis** (11 studies)
- **Developer surveys** (6 studies)
- **Interviews** (14 studies)
- **Commit-derived proxies** (S010 — mining study)

The lack of standardized outcome metrics across studies (Theme T16) means
quantitative comparison across studies is not possible. Most studies report
bespoke metric combinations.

## RQ4: Open challenges

### Methodological challenges

1. **Lack of standardized outcome reporting (13 studies)** — The dominant
   methodological concern. No common framework exists for measuring
   consolidation success, making cross-study comparison impossible.

2. **Short follow-up periods (most studies)** — Only S007 has >5-year
   follow-up. Long-term effects of consolidation are essentially unknown.

3. **Confounder attribution (11 studies)** — Team changes, technology
   upgrades, and market shifts during the same period confound causal
   attribution of outcomes to the consolidation itself.

4. **Self-selection of successful cases (9 studies)** — Published cases
   are predominantly successes. Failed consolidations are under-reported
   in the peer-reviewed literature, creating a significant publication
   bias risk.

### Practice challenges

5. **DDD expertise barrier** — Studies using bounded-context alignment
   (T08) emphasize that DDD expertise is required. Teams without this
   expertise cannot use this strategy successfully.

6. **Peak-load ceiling** — S001 explicitly notes that post-consolidation,
   the monolith has a scaling ceiling the distributed architecture did
   not. Future research should characterize when this ceiling becomes
   binding.

## Cross-cutting observations

The field is in an empirical catch-up phase: practitioner experience is
ahead of academic synthesis. The 23 included studies cluster heavily
around 2023-2025, suggesting the academic community is rapidly catching up
to industry reports like the CNCF 2025 consolidation survey.

Two research gaps stand out as most urgent: (1) standardized outcome
metrics for cross-study synthesis, and (2) long-term longitudinal studies
beyond the typical 12-18 month follow-up.
