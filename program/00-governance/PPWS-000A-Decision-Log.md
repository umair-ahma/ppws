# Program Decision Log

> **Document ID:** PPWS-000A
> **Layer:** Governance
> **Status:** `DRAFT`
> **Depends on:** PPWS-001
> **Primary author:** AI research agent  ·  **Human reviewer/sign-off:** TBD (verify-async; see PPWS-000D)
> **Target length / acceptance criteria:** see `../../initial_plan.md`

## Purpose
Append-only record of binding program decisions, each with date, rationale, and
downstream impact. Decisions are **not** silently reversed: a superseding entry
is appended and the original is marked `SUPERSEDED`. This log is the single
source of truth for "why is the program built this way?"

**Legend — Status:** `ACTIVE` · `SUPERSEDED` · `PROPOSED`
**Legend — Origin:** 👤 owner decision · 🤖 agent recommendation accepted · 🔬 assessment-driven

---

## D-0001 — Sampling honesty pivot 👤 `ACTIVE`
- **Date:** 2026-06-06
- **Decision:** Abandon any "nationally representative probability sample" claim.
  Adopt a **frame / venue / network sample** of professional women drawn through
  professional bodies, employer HR, alumni and professional networks, with
  **quota controls** (province, sector, age band, marital cohort) and
  **post-stratification weighting** to known margins (LFS/PSLM female
  graduate-employment distributions).
- **Rationale:** No enumerable sampling frame exists for "Pakistani women, 25+,
  BA+, employed" (a few percent of women); probability sampling would multiply
  cost and timeline. The owner accepts the trade-off: *"drop high cost
  probability sampling, professional women are mostly in urban centers anyway,
  lets find the best frame/quota and weighting design."*
- **Downstream impact:** PPWS-003 (Methodology), PPWS-009B (Fieldwork/Sampling
  Ops), PPWS-004 (planned-missingness design), all funding documents. Claim
  language standardizes to *"a large, sector-stratified sample of professional
  women,"* never *"nationally representative."*

## D-0002 — Religious & Spiritual Ecology becomes a dedicated ontology domain 👤 `ACTIVE`
- **Date:** 2026-06-06
- **Decision:** Promote **Religious & Spiritual Ecology** to its own ontology
  domain (**Domain J**), inserted immediately after **Cultural Ecology (I)** and
  before **Workplace Ecology**. This shifts the previously sketched letters:
  Workplace J→**K**, Personal Agency K→**L**, Mental Wellbeing L→**M**, Physical
  Wellbeing M→**N**, Life Satisfaction N→**O**, Future Orientation O→**P**. The
  ontology now spans **16 domains, A–P**.
- **Rationale:** Owner: *"spirituality plays a huge part in overall life
  satisfaction … we can't divorce religion from culture, especially in Pakistan
  … all dating sites use religious information to match people, it plays a part
  in a person's identity … go ahead with a full ontology setup for religious
  biases."* Folding religion into Culture/Identity would prevent it from
  functioning as a discrete latent construct in the SEM. It is kept *adjacent*
  to Cultural Ecology and cross-linked to Identity to preserve the conceptual
  tie without losing discreteness.
- **Downstream impact:** PPWS-000B (taxonomy), PPWS-001A / 001A-1 / 001A-2
  (ontology), PPWS-001B (variable dictionary), PPWS-001D (a religiosity construct
  available as predictor/moderator), instruments (a spirituality/religiosity
  sub-module and rating items), `initial_plan.md` §4 taxonomy table.

## D-0003 — English-only at launch 👤 `ACTIVE`
- **Date:** 2026-06-06
- **Decision:** Launch instruments in **English only**. Urdu and regional-language
  translation are **out of scope** for the first wave.
- **Rationale:** Owner: *"English only."* The target population (BA+ professional
  women in urban centres) is functionally English-literate; this removes the
  forward/back-translation critical-path item and cognitive-testing-in-multiple-
  languages cost.
- **Downstream impact:** PPWS-004L (Translation Protocol) is **deferred / parked**
  (kept as a placeholder for a future wave, not built now); consent forms simplify
  to English; timeline and budget drop the translation line. *Supersedes the
  "Urdu + English first" assumption in `initial_plan.md` §3.5 and §11.5.*

## D-0004 — Women-only; no comparison/longitudinal pre-build 👤 `ACTIVE`
- **Date:** 2026-06-06
- **Decision:** Instruments and design target **women only**. Do **not** add work
  now to make instruments reusable for a future male comparison cohort or a
  longitudinal follow-up.
- **Rationale:** Owner: *"dont add extra work, its for women only."*
- **Downstream impact:** Removes dual-cohort wording from instruments and SAP;
  the comparative framework remains *within-women* (Cohort A married vs Cohort B
  not-currently-married), not women-vs-men.

## D-0005 — Funding posture: international-only, process-first 👤 `ACTIVE`
- **Date:** 2026-06-06
- **Decision:** Target **international funders only**. No domestic-only constraint.
  No leads yet — therefore build a **repeatable funder-discovery and outreach
  process** rather than chase a single named grant. Owner seeds basic technical
  bills from personal savings; **detailed budget planning is deferred** until a
  concrete operating system exists.
- **Rationale:** Owner: *"no leads yet, lets make a process for finding those, Im
  gonna go for international funding only"* and *"I am going to delay the budget
  planning until I have a concrete operating system in place."*
- **Downstream impact:** PPWS-011/011A (funding strategy + funder landscape) becomes
  a **process and pipeline** document; PPWS-010* budget tiers stay as scaffolding
  with indicative figures only until activated.

## D-0006 — Institutional host: none yet; secure-a-host plan required 👤 `ACTIVE`
- **Date:** 2026-06-06
- **Decision:** No institutional host secured. Add a **host-acquisition workstream**
  to the process flow (a university or research NGO that can hold a grant and
  provide IRB).
- **Rationale:** Owner: *"Not yet, add to process flow … we need a plan to secure
  one."*
- **Downstream impact:** PPWS-011D (Institutional Host & PI Plan) owns this
  workstream; ethics package (PPWS-008) flags host-IRB as a dependency/risk.

## D-0007 — Named PI: recruit a PI who also supervises owner's MS→PhD 👤 `ACTIVE`
- **Date:** 2026-06-06
- **Decision:** Recruiting a credentialed PI is **part of the task**. Preferred
  profile: a PI who can **also serve as academic supervisor**, enabling the owner
  to convert parts of this program into an **MS-by-thesis** and ultimately a
  **PhD**.
- **Rationale:** Owner: *"Thats part of the task. Im thinking to find a good PI who
  can also serve as a supervisor and I use some parts of this program to get a MS
  degree by thesis only, and eventially a Phd too."*
- **Downstream impact:** PPWS-011D PI plan adds supervisor-fit and
  degree-pathway criteria to the PI search rubric.

## D-0008 — Autonomous agents + asynchronous review files 👤 `ACTIVE`
- **Date:** 2026-06-06
- **Decision:** AI agents are **fully autonomous**: they complete and commit work
  **without waiting** for sign-off. When questions/assumptions exist, the agent
  emits a **topic-named review file** (e.g. `ontology_review.md`,
  `instrument_review.md`) in the repo root **and/or** the PR description, listing
  every open question and concern. Humans verify asynchronously; no work is
  bottlenecked on review.
- **Rationale:** Owner: *"Agents are fully autonomous they complete their work and
  dont wait for a sign off. However, they create a review file when needed … they
  ask all the questions and write all the concerns."* This refines the earlier
  "human gate before APPROVED" rule: the **gate still exists for verification of
  citations/figures/legal-ethics claims**, but it is a *post-hoc verification*
  gate, not a *blocking* gate.
- **Downstream impact:** PPWS-000C / PPWS-000D operating model updated; every
  authoring task ships a `*_review.md` when it makes non-trivial assumptions.

## D-0009 — Markdown-only repository, APA style 👤 `ACTIVE`
- **Date:** 2026-06-06
- **Decision:** All deliverables stay **Markdown** in this repo (LLM-readable,
  Obsidian-mappable, portable). Exports to PDF/Word are done **manually by the
  owner** when needed. Citation/house style follows **APA** best practice.
- **Rationale:** Owner: *"keep it .md so all my LLMs can read it, my Obsidian can
  read and create a map … use the best practices and acceptable standards"* (APA).
- **Downstream impact:** No build pipeline for PDFs; PPWS-002/002A and all cited
  documents use APA author–date in text with a reference list.

## D-0010 — Begin authoring highest-leverage documents (foundation first) 👤 `ACTIVE`
- **Date:** 2026-06-06
- **Decision:** Move from scaffolding to **authoring**, starting with the
  **Foundation Layer ontology** (master + A–E migration + F–P), then the
  literature-review strategy.
- **Rationale:** Owner: *"good job, now make sure to track these files … Lets begin
  working on the foundation first. complete the ontology in the light of new
  information."*
- **Downstream impact:** Index statuses for foundation ontology docs move
  `NOT STARTED → DRAFT`; registries kept in sync per owner's tracking instruction.

---

## Open decisions awaiting owner input (tracked, non-blocking)
These are surfaced in `ontology_review.md` and do not block downstream work; a
defensible default is in force until the owner rules.

| Ref | Question | Working default |
|---|---|---|
| OD-1 | Which 2–4 confirmatory SEM models are the flagship findings? | Candidate set H1–H6 drafted in `ontology_review.md`; owner to pick/tweak. |
| OD-2 | Confirm target **N ≈ 2,000**, online-first first wave? | Proceeding on N≈2,000 online-first until changed. |
| OD-3 | Pilot-tier budget envelope | Deferred per D-0005; technical bills self-seeded. |
