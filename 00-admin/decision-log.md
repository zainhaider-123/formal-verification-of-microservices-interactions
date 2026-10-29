# Decision Log

Append-only record of all methodological decisions for transparency and
reproducibility per PRISMA 2020 item 24c (amendments to protocol).

---

## 2026-01-12 — Topic scope definition

**Decision:** Limit scope to peer-reviewed empirical studies reporting on
the consolidation of microservices back to modular monoliths. Exclude
purely conceptual papers, anecdotal blog posts, and marketing content.

**Rationale:** Scoping search returned many opinion pieces and practitioner
blog posts on "microservices vs monolith" debates. Restricting to empirical
studies with documented consolidation cases produces a rigorous, tractable
corpus.

---

## 2026-01-28 — Date range

**Decision:** Restrict search to 2020-2026.

**Rationale:** The explicit "return to monolith" trend gained academic
traction after 2020, following several high-profile industry cases (DHH's
Basecamp rewrite, Amazon Prime Video 2023 case). Pre-2020 work on monolith
decomposition is already covered by earlier reviews.

---

## 2026-02-05 — Language restriction

**Decision:** Include only papers written in English.

**Rationale:** Team has no consistent multi-language capability. Limitation
acknowledged in threats to validity.

---

## 2026-02-15 — Publication types

**Decision:** Include peer-reviewed journal articles and peer-reviewed
conference papers at CORE A* and A ranked venues. Exclude industry whitepapers,
blog posts, theses, and workshop papers under four pages.

**Rationale:** This topic has abundant grey literature but we require peer
review as a quality floor. CORE A*/A cutoff is objective and replicable.

---

## 2026-03-02 — Search string finalization

**Decision:** Final canonical search string locked after pilot returned 847
Scopus records. Terms "modular monolith," "modulith," and "service
consolidation" proved most discriminating. String saved in
`02-searches/search-string-canonical.txt`.

---

## 2026-04-05 — Screening tool

**Decision:** Use Rayyan for dual-independent screening with reviewer
blinding enabled.

**Rationale:** Rayyan supports the dual-independent screening workflow with
reviewer blinding per PRISMA 2020 item 8.
