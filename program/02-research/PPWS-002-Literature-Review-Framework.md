# Literature Review Framework & Research-Assistant Strategy

> **Document ID:** PPWS-002
> **Layer:** Research
> **Status:** `DRAFT`
> **Depends on:** PPWS-001, PPWS-001A (ontology A–P), PPWS-001D
> **Primary author:** AI research agent  ·  **Human reviewer/sign-off:** TBD (verify-async; see PPWS-000D)
> **Audience:** the assigned **Research Assistant (RA)** + PI
> **Style:** APA 7th edition (Decision D-0009)

## Purpose
A **ready-to-assign strategy** the owner can hand to a research assistant to
produce the literature review — the program's single biggest credibility gap.
It defines scope, search protocol, screening rules, the evidence-matrix workflow
(`PPWS-002A`), the synthesis structure, citation standards, and a concrete
work-plan with deliverables. It is organized **around the 16 ontology domains
(A–P)** so every measured construct is evidence-backed and every gap claim is
sourced.

> **Hard rule (D-0008 verification gate):** every citation must be **real and
> verifiable** — no fabricated or "approximate" references. The RA records a
> resolvable identifier (DOI/handle/stable URL) for each source. AI assistance
> may draft synthesis text, but a human verifies every reference.

---

## 1. Objectives
1. **Justify each construct:** show, per domain (A–P), that the constructs we
   measure are established in the literature (or flag where we innovate — e.g.
   the discrete **Religious & Spiritual Ecology (J)** treatment).
2. **Establish the gap empirically:** position PPWS against national datasets
   (PSLM/PDHS/LFS) and prior gender/work/wellbeing studies on Pakistani and
   comparable South-Asian/MENA professional women.
3. **Source the theory:** ground the nine charter theories (Gender Role, Social
   Identity, Role Congruity, Family Systems, Ecological Systems,
   Self-Determination, Human Capital, Intersectionality, Life Course).
4. **Inform instruments:** identify **validated scales** (DASS-21, SWLS,
   Rosenberg, CD-RISC, autonomy and religiosity/spiritual-wellbeing scales) and
   their psychometrics in South-Asian/Muslim-majority samples (feeds PPWS-004K).
5. **Calibrate priors:** extract effect sizes / prevalences to inform the
   synthetic-data priors (PPWS-006) and the SEM power analysis (PPWS-001D).

## 2. Scope & boundaries
- **In scope:** educated/professional women; marriage & family pressure; women's
  workforce participation, workplace bias and equity; caregiving burden; agency/
  autonomy; mental, physical, and spiritual wellbeing; life satisfaction; religion
  & gender; relevant validated instruments — focused on **Pakistan first**, then
  **South Asia / Muslim-majority / global** as comparators.
- **Out of scope (now):** non-professional/rural-only samples except as
  comparators; male-only studies except where they frame women's outcomes;
  non-English instruments work (English-only launch, D-0003).
- **Recency:** prioritize **2010–present**; include seminal older work for theory.

## 3. Search protocol (reproducible)
**Databases/sources:** Google Scholar, Scopus, Web of Science, PubMed/PsycINFO,
JSTOR; **grey literature** (HEC repository, UN Women, World Bank, ILO, PBS/PSLM,
NIPS/PDHS, PIDE, LUMS/IBA working papers). Record the database, date, and exact
query string for each search (reproducibility).

**Query building blocks (combine with AND/OR; adapt per database):**
- Population: `("professional women" OR "working women" OR "educated women" OR "career women")`
- Place: `(Pakistan OR "South Asia" OR Muslim OR Islamic OR MENA)`
- Construct (rotate per domain): e.g. `("marriage pressure" OR "marital expectations")`,
  `("work-family conflict")`, `("women's autonomy" OR agency)`, `("religiosity" OR spirituality OR "religious coping")`,
  `("workplace discrimination" OR "gender bias")`, `("life satisfaction" OR wellbeing OR "mental health")`,
  `(caregiving OR "elder care")`.

**Per-domain coverage matrix (assign one query set per domain A–P):** the RA runs
at least one structured search **per ontology domain**, guaranteeing no construct
is left unsupported. Domain J (Religious & Spiritual) gets dedicated searches on
religiosity measurement, religious coping, and religion–gender-role attitudes.

## 4. Screening & inclusion (PRISMA-style)
1. **Identification:** export all hits to the reference manager (Zotero
   recommended — open, exports APA + BibTeX).
2. **De-duplicate.**
3. **Title/abstract screen** against inclusion criteria (population + construct +
   relevance). Record include/exclude + reason.
4. **Full-text screen** of survivors; confirm a resolvable identifier exists.
5. **Log counts** at each stage (a simple PRISMA flow: identified → screened →
   included). Target **≈ 60–120 included sources** for a credible review.

**Quality appraisal (lightweight):** tag each included source by design
(national survey, peer-reviewed empirical, qualitative, review/meta-analysis,
grey/report) and note sample, country, and key limitation.

## 5. The evidence matrix — `PPWS-002A` (the RA's core deliverable)
Every included source becomes one row in `PPWS-002A-Literature-Matrix.md`:

| Column | Content |
|---|---|
| Citation (APA) | Full APA 7 reference |
| Identifier | DOI / stable URL / handle |
| Country & population | e.g. Pakistan, urban professional women |
| Design & N | e.g. cross-sectional survey, N=420 |
| Construct(s) | Mapped to ontology domain letter(s) **A–P** |
| Key finding | 1–2 sentences (effect size/prevalence if given) |
| Instrument used | Named scale + reliability if reported |
| Gap addressed | Which PPWS gap/RQ this informs |
| Quality/limitation | Brief note |

The matrix is the bridge from raw sources to the narrative and feeds priors
(PPWS-006) and the scales register (PPWS-004K).

## 6. Synthesis structure (the written review)
Organize the narrative as:
1. **Context & gap** — Pakistani women's education vs labour-force participation;
   what PSLM/PDHS/LFS do and do **not** capture about *professional* women
   (justifies a bespoke study).
2. **Thematic synthesis by domain cluster:** (i) Family/Relationship/Parenthood/
   Caregiving load (B–E); (ii) Professional/Economic/Workplace position (F, G, K);
   (iii) Social/Cultural/**Religious** environment (H, I, **J**); (iv) Agency as
   mediator (L); (v) Wellbeing & life-satisfaction outcomes (M, N, O, P).
3. **Theoretical integration** — tie findings to the nine theories.
4. **Instrumentation review** — validated scales and their psychometrics in
   comparable samples.
5. **Synthesis of gaps → RQs** — show each RQ/hypothesis (H1–H7, `ontology_review.md`)
   is literature-motivated.

## 7. Citation & integrity standards (APA 7)
- In-text author–date; full reference list; **every** in-text cite resolvable in
  the matrix. No citation without a verified identifier. Quote sparingly; never
  fabricate page numbers, DOIs, or findings.
- Maintain the Zotero library + an exported `.bib`/APA list committed alongside
  the review.

## 8. RA work-plan & deliverables (assignable)
| Stage | Deliverable | Done-when |
|---|---|---|
| W1 | Search log (queries per domain A–P) + Zotero library seeded | ≥1 structured search per domain logged |
| W2 | Screening complete + PRISMA counts | Title/abstract + full-text screens logged |
| W3 | `PPWS-002A` evidence matrix populated | ≥60 verified rows, each mapped to a domain |
| W4 | Draft synthesis §1–§3 | Gap + thematic + theory sections drafted |
| W5 | Draft synthesis §4–§5 + reference list | Instruments + gaps→RQs; APA list complete |
| W6 | Revision after PI verification | All citations human-verified; gaps evidenced |

*(Stage labels are sequence markers, not fixed calendar weeks.)*

## 9. Acceptance criteria (from `initial_plan.md` §9)
- Every gap claim is evidenced; **no fabricated references**.
- Each ontology domain A–P has ≥1 supporting source in the matrix.
- Validated-scale choices are justified with psychometric evidence (feeds 004K).
- Positions PPWS explicitly against PSLM/PDHS/LFS.

## 10. Handover notes for the RA
- Read first: `PPWS-001A` (ontology overview) + this file + `ontology_review.md`.
- Work in **Markdown** only; cite in **APA**; keep the Zotero library current.
- Raise questions in a `literature_review_notes.md` (mirrors the agent
  review-file convention, D-0008) rather than blocking.

## Cross-references
- Evidence matrix template & rows: `PPWS-002A-Literature-Matrix.md`.
- Constructs to support: `../01-foundation/PPWS-001A-*` (domains A–P).
- Scale permissions: `../03-instruments/PPWS-004K-Validated-Scales-Register-and-Permissions.md`.

## Change log
- 2026-06-06 — Authored as an assignable RA strategy; organized around the 16-domain
  A–P ontology (incl. Religious & Spiritual J); APA + verifiable-citation rules.
  Status `DRAFT`.
