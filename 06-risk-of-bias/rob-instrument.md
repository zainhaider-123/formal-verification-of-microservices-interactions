# Risk of Bias Assessment Instrument

A custom instrument for empirical software engineering case studies on
microservices consolidation, addressing PRISMA 2020 item 11. Adapted from
QUADAS-2 principles (Whiting et al., Ann Intern Med 2011) with items
specific to software architecture case study research.

Each domain is rated:
- **Low risk** — Sufficient information; methodology sound
- **Some concerns** — Information incomplete or methodology has minor issues
- **High risk** — Significant methodological weakness

Studies with two or more "high risk" ratings are flagged for sensitivity
analysis but are NOT excluded from synthesis (per PRISMA 2020, risk of bias
informs interpretation, not inclusion).

## Domains

### D1. Case selection bias
Is the case (or cases) selected in a way that avoids cherry-picking? Is the
sampling strategy documented?

**Low risk:** Purposive sampling documented with rationale, or census of a
well-defined population
**Some concerns:** Convenience sampling acknowledged
**High risk:** Single successful case with no selection justification

### D2. Data collection rigor
Is the data collection method systematic and triangulated across sources?

**Low risk:** Multiple data sources triangulated (interviews + documents +
metrics)
**Some concerns:** One or two sources without triangulation
**High risk:** Anecdotal reporting, single source, no collection protocol

### D3. Measurement validity
Are outcome measurements defined, appropriate, and captured with enough
rigor to be trusted?

**Low risk:** Pre-defined outcomes, operationalized metrics, baseline
captured before change
**Some concerns:** Some outcomes measured post-hoc
**High risk:** All outcomes self-reported post-hoc without baselines

### D4. Confounding control
Are competing explanations for observed outcomes considered and controlled?
(E.g., team changes during the same period, technology upgrades, market shifts.)

**Low risk:** Confounders identified and addressed (statistically or
qualitatively)
**Some concerns:** Confounders mentioned but not addressed
**High risk:** No discussion of alternative explanations

### D5. Researcher-practitioner bias
Is there potential bias from the researchers being employed by the
organization being studied?

**Low risk:** Independent researchers or reflexivity explicitly addressed
**Some concerns:** Authors employed by the company but with declared
reflexivity
**High risk:** Authors employed, no declared reflexivity, promotional tone

### D6. Reporting completeness
Are methods reported in sufficient detail for reproducibility? Are negative
findings reported alongside positive ones?

**Low risk:** Full method reporting, negative findings included, replication
package
**Some concerns:** Methods partial; some selective reporting
**High risk:** Methods vague; evident selective reporting

## Overall risk of bias

- All domains "Low risk" → **Low overall**
- One "High risk" or several "Some concerns" → **Some concerns overall**
- Two or more "High risk" → **High overall**

## Process

1. R1 assesses all included studies independently.
2. R2 independently assesses a 50% random sample.
3. Disagreements are discussed; persistent disagreements escalated.
4. Cohen's kappa is calculated on the sample.
