# PPWS — Initial Program Plan (`initial_plan.md`)

**Program:** Pakistan Professional Women Study (PPWS)
**Document type:** Master build plan / program operating plan
**Prepared:** 2026-06-06
**Inputs digested:** `context/opus4.8_assessment.md`; `source/PPWS-001-Research-Charter.md`; `source/PAKISTAN PROFESSIONAL WOMEN STUDY (PPWS).docx.md`; `source/Executive Summary.md`; `source/PPWS addendums.md`
**Companion artifacts created with this plan:** `program/` (full pre-allocated document stack), `program/PPWS-000-Program-Index.md` (live registry), `program/README.md`.

> **How to read this file.** Sections 1–4 establish *where we are* and *the binding decisions*. Section 5 is the **document stack** (what to build). Section 6 is the **phased roadmap** (in what order). Section 7 is the **AI-agent + in-house operating model** (who/what does the work). Section 8 is **funding**. Section 9 is per-document **acceptance specs**. Section 10 is **risks**. Section 11 is **open questions I need you to answer** — these change the plan materially, so please respond to them.

---

## 1. Executive orientation

The PPWS corpus is **not a codebase**; it is the founding document set of a national social-science research institute-in-waiting. Four documents currently exist in mixed maturity:

| File | What it is | Maturity |
|---|---|---|
| `PAKISTAN PROFESSIONAL WOMEN STUDY (PPWS).docx.md` | Clean Research Charter v3.0 (vision, scope, population, cohorts, 15 domains, 9 theories, 8 RQs, 7-phase method) | Solid blueprint |
| `PPWS-001-Research-Charter.md` | Same charter **plus** Measurement Ontology Part 1 (Domains A–E, ~60 variables fully specified) | **Strongest asset** |
| `Executive Summary.md` | Operational supplement: governance, deliverables, risk register, ethics, sampling/power, fieldwork SOP, instrument plan, synthetic-data model, SAP, budget (~PKR 6.85M), 18-month Gantt | Strong but figures are placeholder |
| `PPWS addendums.md` | Raw thinking-output: why ontology precedes questionnaires, Domains A–O sketch, master causal chain, primary outcomes, and the **build order of ~19 documents (300–500+ pp)** | Scaffolding / meta-plan |

**The single most important truth in the corpus** (and its genuine competitive advantage) is the *ontology-first* discipline:

```
Charter → Measurement Ontology → Variable Dictionary → Dataset Schema →
Causal Model → Research Questions → Questionnaires → Statistical Models
```

Defining *what reality to measure* before writing questions is what separates an instrument suite engineered to test a pre-specified causal model (via SEM) from a survey that accidentally produces correlations. The hardest and rarest intellectual work — deciding *what to measure and why* — is **largely done and done well**. What remains is mostly **production and discipline, not invention**, which is precisely the kind of work expert LLM agents can execute at scale.

---

## 2. Where we honestly stand (the assessment, distilled)

The independent expert review (`opus4.8_assessment.md`) graded the corpus against three bars:

- **(A) Sufficient for a funded research *center*?** Not yet. But it is the right *kind* of foundation and unusually strong at the conceptual layer.
  - Fundable **concept note** (5–15 pp): **~80% there.**
  - Fundable **full grant proposal**: **~35–45% there.**
  - Operating **research center**: **~15–20% there.**
- **(B) Actually possible in practice?** **Yes — but only at a deliberately scoped version of itself.** The *literal* monolithic design (national probability sample of a rare population, 15 domains, 300–500 variables, full SEM, 7 regions, multi-language, 18 months, USD 25k) is **not simultaneously achievable**. A **staged, honestly-scoped** version is very achievable and still scientifically valuable.
- **(C) Next steps?** Finish the **Foundation Layer** first (desk work, doable now), then add the **literature review** and a **demonstrated pilot**, name a **PI + host**, rebuild the **budget into tiers**, and pursue funding in **stages**.

### The eight gaps that block a *full* proposal (from the assessment)
1. Literature review with **real citations** (currently near-absent).
2. **Complete** Measurement Ontology (only A–E of A–O exist).
3. **Actual instruments** (no finalized items, no named validated scales + permissions, no Urdu translation/back-translation, no cognitive testing).
4. **Ethics/IRB package** (described in prose, not produced).
5. **Sampling-frame realism** (no usable frame for this rare subpopulation).
6. **Credible, costed budget** (PKR 6.85M / ~USD 25k is implausibly low — likely 3–6× too small).
7. **Team & institutional home** (no named PI, no host, no letters of support).
8. **Power analysis tied to the actual SEM** (current justification is generic).

---

## 3. The five binding strategic decisions (resolve these first; they propagate everywhere)

These are the load-bearing decisions. They belong in `program/00-governance/PPWS-000A-Decision-Log.md`. Recommended resolutions are pre-filled; items flagged **⚠ needs your call** are in Section 11.

1. **Sampling honesty pivot — the most important single decision.**
   Abandon the "nationally representative probability sample" claim. There is **no sampling frame** for "Pakistani women, 25+, BA+, employed" (a few percent of women; not enumerable from census blocks without enormous screening cost). **Adopt a frame/venue/network sample** via professional bodies (PEC, PMDC/PMC, PBC/bar councils, ICAP/ICMA, HEC faculty lists, chambers of commerce, large-employer HR, alumni/LinkedIn networks) with **quota controls** (province, sector, age, marital cohort) and **post-stratification weighting** to known margins (LFS/PSLM female-graduate-employment distributions). Claim *"a large, sector-stratified sample of professional women,"* **not** *"nationally representative."*

2. **Instrument length → core + rotating modules.**
   15 domains × multiple scales = a 30–60 minute instrument where data quality collapses. Define a **core module (~15–20 min)**: demographics, cohort variables, the 5 primary outcomes, and key mediators; push the rest into **rotating/optional modules** via **planned-missingness (matrix sampling)** so no respondent sees everything.

3. **SEM scope → 2–4 pre-registered focused models, not one mega-graph.**
   N≈2,000 supports *focused* confirmatory models (e.g., *Family Pressure → Agency → Psychological Wellbeing → Life Satisfaction*, moderated by *Economic Independence*), not a 15-construct everything-causes-everything DAG. Keep the ontology comprehensive but the confirmatory models small and theory-driven.

4. **Budget → three costed tiers, executed in sequence.**
   Replace the single implausible figure with **Pilot (~USD 15–40k) → Regional (~USD 80–150k) → National-ambition (USD 300k+)**. Treat the existing PKR 6.85M as a *pilot-tier* figure only.

5. **Timeline realism → IRB + translation on the critical path.**
   The 18-month Gantt is optimistic once NBC-REC + institutional IRB are included. **Launch is English-only (Decision D-0003)**, which removes translation from the critical path; phase regions (**Karachi, Lahore, Islamabad/Rawalpindi first**), and start IRB early.

---

## 4. Naming, taxonomy, and de-duplication (Phase 0 housekeeping)

- **One canonical charter.** `docx.md` and `PPWS-001` duplicate the charter. Merge into a single authoritative `program/00-governance/PPWS-001-Research-Charter.md`; retire the divergence under version control.
- **Reconcile the two domain numberings.** The charter uses **15 numbered domains**; the ontology uses **A–P** (16 domains, after promoting Religious & Spiritual to its own Domain J — D-0002). One mapped taxonomy ensures "Domain 11" and "Domain K" never confuse a reader. Mapping (ratified in `PPWS-000B`):

  | Ontology | Domain | Charter # (closest) |
  |---|---|---|
  | A | Identity & Demographics | 1 |
  | B | Family Ecology | 4 |
  | C | Relationship Ecology | 5 |
  | D | Parenthood Ecology | 6 |
  | E | Caregiving Ecology | 7 |
  | F | Professional Ecology | 2 |
  | G | Economic Ecology | 3 |
  | H | Social Ecology | 8 |
  | I | Cultural Ecology | 9 |
  | **J** | **Religious & Spiritual Ecology** (new — D-0002) | **10** |
  | K | Workplace Ecology | 11 |
  | L | Personal Agency | 12 |
  | M | Mental Wellbeing | 13 |
  | N | Physical Wellbeing | 14 |
  | O | Life Satisfaction | 15 (part) |
  | P | Future Orientation | 15 (part) |

  *Resolved (Decision **D-0002**):* the charter's **Domain 10 (Religious Context)**
  is now its **own ontology domain J** (Religious & Spiritual Ecology), inserted
  after Cultural Ecology (I); former J–O shift to **K–P**. The ontology now spans
  **16 domains, A–P**. Ratified in `PPWS-000B`; see `PPWS-000A` D-0002.

- **Document ID convention:** `PPWS-<NNN><letter?>-<Short-Title>.md`. Numbers encode build order; letters encode parts/children.
- **Status lifecycle:** `NOT STARTED → DRAFT → IN REVIEW → APPROVED → FROZEN`.

---

## 5. The full document stack (what gets built)

The pre-allocated files already exist as placeholders under `program/`. The live registry with dependencies and status is `program/PPWS-000-Program-Index.md`. Layers:

- **Governance** (`00-governance/`): canonical charter, decision log, taxonomy, version-control protocol, **AI-agent operating model**.
- **Foundation** (`01-foundation/`): ontology master (A–P) + Part 1 (A–E) + Part 2 (F–P, incl. new Religious & Spiritual J), variable dictionary, dataset schema, causal/SEM model. **← highest leverage.**
- **Research** (`02-research/`): literature review framework + evidence matrix, research methodology.
- **Instrument** (`03-instruments/`): questionnaire system master + 9 scale modules + interview guide + validated-scales register/permissions + translation protocol.
- **Analytics** (`04-analytics/`): scoring manual, synthetic-data framework, SAP, plus reproducible `analysis/*.R` and `synthetic-data/generate_synthetic.R` script stubs.
- **Ethics** (`05-ethics-governance/`): IRB package, consent forms (EN/UR), data management/protection, anonymization/sharing.
- **Operations** (`06-operations/`): project plan, risk register, fieldwork SOP, three-tier budget.
- **Funding** (`07-funding/`): funding strategy, funder landscape, concept note, full-proposal template, PI/host plan.
- **Dissemination** (`08-dissemination/`): dissemination & impact plan, policy-brief template.

This expands the addendum's ~19-document list to ~30 files by adding the **governance, ethics, operations, and funding** artifacts the assessment shows are required for a *fundable* program (the addendum focused only on the scientific stack).

---

## 6. Phased roadmap (build order)

The ordering front-loads the work that (a) is pure desk work, (b) de-risks feasibility, and (c) wins funding.

### Phase 0 — Consolidate & decide (≈1–2 weeks, desk)
- Merge to one canonical charter (`PPWS-001`).
- Write the five binding decisions into `PPWS-000A-Decision-Log.md` (especially the sampling honesty statement).
- Ratify the unified domain taxonomy (`PPWS-000B`).
- Stand up version-control + the AI-agent operating model (`PPWS-000C`, `PPWS-000D`).

### Phase 1 — Finish the Foundation Layer (makes everything downstream mechanical)
- `PPWS-001A-2` **Ontology Domains F–P** — replicate the A–E specification depth for the remaining 11 domains (now incl. the dedicated Religious & Spiritual Ecology domain J). **This is the single highest-leverage task.** *(authored — `DRAFT`)*
- `PPWS-001B` **Variable Dictionary** — all ~300–500 variables, each tagged CORE vs OPTIONAL.
- `PPWS-001C` **Dataset Schema** — every column/type/key/derivation; generatable from 001B.
- `PPWS-001D` **Causal/SEM Specification** — latent constructs, indicators, mediators, moderators, the 2–4 pre-registered confirmatory models, and the DAG.

### Phase 2 — Evidence & method (what funders score)
- `PPWS-002` **Literature Review** with real citations + `PPWS-002A` evidence matrix. *Biggest credibility gap.*
- `PPWS-003` **Research Methodology** — lock frame/quota + weighting, modes, recruitment, SEM-derived power analysis, planned-missingness design.

### Phase 3 — Instruments (derived from the ontology)
- `PPWS-004` master + `004A–004I` scales, mapping each construct to a validated scale where one exists (DASS-21, SWLS, Rosenberg, Connor-Davidson, …) and authoring new items only where needed.
- `PPWS-004J` interview guide; `PPWS-004K` scales register + permissions; `PPWS-004L` Urdu/English translation (regional languages phased).
- Cognitive testing (~20 respondents) → revision.

### Phase 4 — Analytics de-risking (BEFORE fieldwork)
- `PPWS-006` **Synthetic Data Generator** → N=2,000 mock dataset from documented priors.
- `PPWS-007` **SAP** + reproducible R scripts, fully runnable on synthetic data; pre-register.
- `PPWS-005` **Scoring & Interpretation Manual.**

### Phase 5 — Pilot, then scale
- `PPWS-008` **Ethics/IRB package** (start early — it's on the critical path).
- **Pilot** (N≈100–150, 1–2 cities, online-first) → real Cronbach's α / McDonald's ω + EFA → revise instruments → *demonstrated* reliability.
- Stage the funding ask in tiers (Pilot → Regional → National).

### Parallel, continuous tracks
- **Funding** (`07-funding/`): concept note out early; build funder list; line up PI + host.
- **Operations** (`06-operations/`): keep risk register live; rebuild budget into tiers.

### Concrete "first 90 days"
1. Weeks 1–2: Phase 0 consolidation + sampling honesty statement.
2. Weeks 2–6: Ontology F–P (`001A-2`, done) + Variable Dictionary (`001B`).
3. Weeks 5–8: Dataset Schema (`001C`) + Causal/SEM spec (`001D`) + DAG.
4. Weeks 6–10: Synthetic data generator + SAP scripts running on mock data.
5. Weeks 8–12: Literature review draft + concept note to one seed funder + name PI/host.

---

## 7. AI-agent + in-house team operating model (detailed in `PPWS-000D`)

Per your direction, **the bulk of design and production work is performed by expert LLM agents**, while the **in-house team contributes credentials, review, sign-off, meetings, and networking**. This plan is structured to make that division explicit and safe.

### Division of labour
| Work | Owner | Notes |
|---|---|---|
| Ontology, dictionary, schema, causal model, SAP drafting | **AI agents** | Pure desk work; highest agent leverage |
| Literature synthesis + citation drafting | **AI agents** | **All citations must be human-verified** — agents must not fabricate references |
| Instrument item authoring + translation drafts | **AI agents** | Human bilingual experts verify translations |
| Synthetic data generator + analysis scripts | **AI agents** | Validated on synthetic data before any real data |
| Scientific/ethical sign-off, IRB submission, PI duties | **In-house humans** | Requires credentials + accountability |
| Funder relationships, partnerships, recruitment | **In-house humans** | Networking + institutional standing |
| Final approval of every document | **In-house humans** | Human-in-the-loop gate before `APPROVED`/`FROZEN` |

### Quality gates (every document)
1. **Agent draft** → 2. **Agent self-review against acceptance spec** (Section 9) → 3. **Cross-agent review** (a second agent critiques) → 4. **Human expert review + sign-off** → 5. status `APPROVED`.
- **Hard rule:** no citation, statistic, scale permission, legal/ethics claim, or budget figure reaches `APPROVED` without **human verification**. Agents draft; humans are accountable.

### Roles (human, credential-bearing)
PI; Co-Investigators (survey / qualitative / analysis); a survey methodologist; a Pakistani gender scholar; a psychometrician (the assessment recommends recruiting these 2–3 advisors even informally). The org chart and meeting cadence live in `PPWS-009`.

---

## 8. Funding strategy (detailed in `07-funding/`)

Funding is treated as a **first-class workstream**, not an afterthought.

### Principle: stage the ask; never bet the program on one large grant
Each tier is a **self-contained, publishable unit** that de-risks and credentials the next.

| Tier | Scope | Indicative cost | Funder fit |
|---|---|---|---|
| **Pilot/Proof** | N≈100–150, 1–2 cities, online-first; reliability + EFA | ~USD 15–40k | Seed/concept rounds, university PRF, small foundations |
| **Regional** | 2–3 professional hubs, larger N, core + rotating modules | ~USD 80–150k | HEC, British Academy, IDRC, mid-size foundations |
| **National-ambition** | Multi-region, translation, qualitative, full SEM | USD 300k+ | Gates, Wellcome, UN Women, World Bank/Pakistan |

### Sequence
1. **Now:** polish the **concept note** (`PPWS-011B`) from charter + executive summary (~80% ready) and open conversations with one or two seed funders.
2. **After Phase 1–2 + pilot:** assemble the **full proposal** (`PPWS-011C`) — now backed by a completed foundation, a real literature review, *demonstrated* pilot reliability, an SEM-derived power analysis, a tiered budget, and a named PI/host.
3. **Non-negotiable for real money:** name a **PI** and secure an **institutional host** that can hold the grant and provide IRB (`PPWS-011D`); recruit 2–3 advisory experts; gather letters of support.

### What makes the ask credible (the assessment's signals)
- A **synthetic dataset + tested analysis scripts** before collection (strong funder signal).
- A **demonstrated pilot** (converts "promised" → "demonstrated").
- An **honest sampling claim** (reviewers read the over-claim or the low budget as inexperience).

**⚠ needs your call:** your funding sources, geography (Pakistan-domestic vs international), and whether a host institution already exists (Section 11).

---

## 9. Per-document acceptance specifications

Each placeholder in `program/` is authored to these bars. (Lengths follow the addendum's own estimates where given.)

| Document | Must contain | Acceptance criteria | Indicative length |
|---|---|---|---|
| `PPWS-001` Charter | Vision, mission, scope, population, cohorts, taxonomy, theories, RQs | One canonical version; SC-approved; no divergence | 15–20 pp |
| `PPWS-001A` Ontology (master) | Entities, domains, classifications, latent/observed, mediators/moderators, outcomes, causal assumptions, boundaries, cohorts, diagrams | Covers A–P (incl. Religious & Spiritual J); internally consistent with charter taxonomy | 20–30 pp |
| `PPWS-001A-2` Domains F–P | Each variable: type, definition, question stem, response format, validation, missing codes, derived indices | Matches the depth/format of existing A–E | — |
| `PPWS-001B` Variable Dictionary | name, code, type, range, valid values, missing codes, derivation, source scale, domain; CORE/OPTIONAL tag | Every variable specified; resolves duplicates (e.g., NUM_CHILD A14↔D1) | 60–120 pp |
| `PPWS-001C` Dataset Schema | Every column/type/key/relationship/derivation | Directly generatable from 001B; supports synthetic data | 30–50 pp |
| `PPWS-001D` Causal/SEM Spec | Latent constructs, indicators, mediators, moderators, 2–4 pre-registered models, DAG | Models identified and powered for N≈2,000 | 20–40 pp |
| `PPWS-002` Literature Review | Synthesis with **real citations**, positioned vs PSLM/PDHS/LFS + prior gender work | Every gap claim evidenced; no fabricated references | 30–50 pp |
| `PPWS-003` Methodology | Frame/quota + weighting design, modes, recruitment, SEM-derived power, planned-missingness | IRB-ready; sampling claim defensible | 40–70 pp |
| `PPWS-004*` Instruments | Item-to-construct map, validated-scale mapping + permissions, reverse-coding, skip logic, translations | Core ≤ ~20 min; cognitively tested; α target ≥ 0.70 | 60–100 pp total |
| `PPWS-005` Scoring Manual | Scoring rules, reverse-coding, derived formulas, interpretation bins | Reproducible scoring of synthetic data | 40–60 pp |
| `PPWS-006` Synthetic Data | Documented priors/distributions + generator | Produces N=1k/2k/5k; documented assumptions | — |
| `PPWS-007` SAP | Pre-registered analyses + reproducible R/Stata scripts | Runs end-to-end on synthetic data | — |
| `PPWS-008*` Ethics/IRB | Protocol, consent (EN/UR), data-protection (PECA), anonymization | NBC-REC + institutional IRB submission-ready | — |
| `PPWS-009*` Operations | Org/roles, milestones, risk register, fieldwork SOP, three-tier budget | Timeline has IRB+translation on critical path | — |
| `PPWS-011*` Funding | Strategy, funder list, concept note, full-proposal template, PI/host plan | Concept note submission-ready | — |
| `PPWS-012*` Dissemination | Publications, report, policy briefs, media, open-data deposit | Audience-specific outputs defined | — |

---

## 10. Risk register (top risks, from the assessment)

| Risk | Severity | Fix |
|---|---|---|
| No real sampling frame for the rare target population | **Critical** | Frame/quota via professional bodies + post-stratification weighting; drop "nationally representative" |
| Budget undersized ~3–6× | High | Three costed tiers; current figure is pilot-only |
| Instrument too long (200–500 vars) | High | Core + rotating modules / planned missingness |
| Literature review absent (no citations) | High | Produce `PPWS-002` before any full proposal |
| No named PI / host institution | High (for funding) | Secure both before submitting full proposals |
| SEM over-scoped for N | Medium | 2–4 pre-registered focused models |
| Ontology only 1/3 complete (A–E of A–O) | ~~Medium~~ Resolved | F–P authored to the A–E standard (incl. new Religious domain J); now `DRAFT` |
| 18-month timeline optimistic | Medium | Re-baseline with IRB + translation on critical path |
| **AI-agent factual risk** (fabricated citations/figures) | High | Human verification gate before any document is `APPROVED` |

---

## 11. Open questions — **RESOLVED** (owner answered 2026-06-06)

> **Status:** All 13 questions answered by the owner and ratified in
> `program/00-governance/PPWS-000A-Decision-Log.md` (Decisions **D-0001 – D-0010**).
> The questions are retained below for provenance, each annotated with the
> resolution. Two scientific choices (flagship hypotheses; N/mode confirmation)
> remain owner-selectable and are tracked non-blocking in `ontology_review.md`.

You explicitly invited "any and all questions." These are the decisions I cannot make for you; each materially reshapes downstream documents.

**Scope & scientific design**
1. **Sampling pivot:** Do you accept dropping the "nationally representative" claim in favour of a defensible **frame/quota + weighting** design? (If you insist on probability sampling, the budget and timeline change by a large multiple.)
2. **Religious Context:** Should it become its own ontology domain (a new letter), or stay folded into Culture/Identity? (Affects taxonomy, variables, instruments.)
3. **Primary confirmatory models:** Which 2–4 causal hypotheses are the *flagship* findings you most want to publish? (Drives `PPWS-001D` and the SAP.)
4. **Target N and modes:** Confirm N≈2,000 and an **online-first** posture for the first fundable wave?
5. **Languages at launch:** Urdu + English first, regional languages phased — acceptable?
6. **Comparative/future waves:** Should instruments be built now to be reusable for a future **male comparison cohort** or **longitudinal** follow-up?

**Funding, institution & people**
7. **Funding sources:** What funding are you targeting (HEC, international donors, private foundations, self/seed, university)? Any existing leads or constraints (e.g., must be Pakistan-domestic)?
8. **Institutional host:** Is there a university or research NGO that can hold a grant and provide IRB, or do we need a plan to secure one?
9. **Named PI:** Is there a credentialed PI identified, or is recruiting one part of the task?
10. **Budget envelope:** What is the realistic near-term budget for the **pilot** tier?

**Operating model & repository**
11. **AI-agent autonomy:** How much should agents auto-produce vs. wait for human sign-off at each gate? Confirm the **"agents draft, humans verify all citations/figures/legal-ethics claims"** rule.
12. **Output formats:** Markdown-only in this repo, or also exported PDFs/Word for funders and IRB? Any house style/citation format (APA?) to standardize now?
13. **Placeholder content:** I have created the files as *empty allocated placeholders* (titles + metadata only), per your instruction. Do you want me to now begin **authoring** the highest-leverage documents (start with `PPWS-001A-2` Ontology F–O), or keep everything as scaffolding for now?

### Resolutions (owner answers → decisions)
| # | Question | Owner's resolution | Decision |
|---|---|---|---|
| 1 | Sampling pivot | **Yes** — drop probability sampling; use frame/quota + weighting | D-0001 |
| 2 | Religious Context | **Own ontology domain** (Domain J), detailed, kept adjacent to culture/identity; full setup | D-0002 |
| 3 | Flagship models | Owner to **pick from drafted candidates** (H1–H7 in `ontology_review.md`) | OD-1 (open) |
| 4 | Target N / mode | Default **N≈2,000, online-first** in force until changed | OD-2 (open) |
| 5 | Languages | **English only** (Urdu/regional deferred) | D-0003 |
| 6 | Comparative/future waves | **No** male-cohort/longitudinal pre-build; women only | D-0004 |
| 7 | Funding sources | **International only**; no leads → build a discovery process | D-0005 |
| 8 | Institutional host | **None yet**; add host-acquisition workstream | D-0006 |
| 9 | Named PI | **Recruit one** who can also be owner's MS/PhD supervisor | D-0007 |
| 10 | Budget envelope | **Deferred**; technical bills self-seeded | D-0005 / OD-3 |
| 11 | AI-agent autonomy | **Fully autonomous**; emit `*_review.md`; verify async (no blocking) | D-0008 |
| 12 | Output formats | **Markdown only**; APA style; owner ports PDFs/Word manually | D-0009 |
| 13 | Begin authoring | **Yes** — foundation first; ontology authored, registries tracked | D-0010 |

---

*This plan operationalizes the assessment's verdicts (A/B/C) into a concrete, dependency-ordered build with pre-allocated files. The intellectual core is strong; the remaining work is production and discipline — well-suited to expert AI agents under human verification.*
