# AI-Agent + In-House Team Operating Model

> **Document ID:** PPWS-000D
> **Layer:** Governance
> **Status:** `DRAFT`
> **Depends on:** PPWS-000C
> **Primary author:** AI research agent  ·  **Human reviewer/sign-off:** TBD (verify-async)
> **Target length / acceptance criteria:** see `../../initial_plan.md`

## Purpose
Defines how expert LLM agents perform the bulk of design/production work while the
in-house team provides credentials, review, sign-off, and networking. **Updated
per Decision D-0008:** agents are **autonomous** and do **not** block on sign-off;
verification is **post-hoc and asynchronous**.

---

## 1. Operating principle — autonomous draft, asynchronous verification
- **Agents are fully autonomous.** They complete and **commit** their work
  without waiting for approval. Work ships in status `DRAFT`.
- **No human bottleneck.** Downstream work may proceed on committed drafts.
- **Verification still happens — just not as a gate that blocks production.** The
  human-in-the-loop **verification** of citations, figures, scale permissions,
  legal/ethics claims, and budget numbers remains mandatory **before a document
  is promoted to `APPROVED`/`FROZEN`**, but it never blocks drafting or dependent
  work.

## 2. The review-file convention (how agents surface concerns)
When an agent makes non-trivial assumptions or has open questions, it emits a
**topic-named review file** in the repo root (and/or the PR description):

- Examples: `ontology_review.md`, `instrument_review.md`, `methodology_review.md`.
- Contents: every assumption made, every open question, the working default in
  force, and a pointer to the affected documents.
- Purpose: humans verify **asynchronously**; the agent does not wait.

> This operationalizes the owner's rule: *"Agents are fully autonomous … they
> create a review file when needed … they ask all the questions and write all the
> concerns. This way, humans will verify all the work, but no work will be
> bottlenecked by human reviews."*

## 3. Division of labour
| Work | Owner | Notes |
|---|---|---|
| Ontology, dictionary, schema, causal model, SAP drafting | **AI agents** | Highest agent leverage; ship as DRAFT |
| Literature synthesis + citation drafting | **AI agents** | **All citations human-verified before APPROVED** — never fabricate |
| Instrument item authoring | **AI agents** | English-only (D-0003); permissions verified by humans |
| Synthetic data generator + analysis scripts | **AI agents** | Validated on synthetic data before any real data |
| Scientific/ethical sign-off, IRB submission, PI duties | **In-house humans** | Credentials + accountability |
| Funder relationships, host, recruitment | **In-house humans** | Networking + standing (D-0005/006/007) |
| **Verification** of citations/figures/legal-ethics/budget | **In-house humans** | Post-hoc gate before `APPROVED`/`FROZEN` |

## 4. Status lifecycle & the verification gate
`NOT STARTED → DRAFT (agent, autonomous) → IN REVIEW (human verifying async) → APPROVED → FROZEN`
- Agents move docs to `DRAFT` freely.
- Promotion to `APPROVED` requires a human to have verified all
  citations/figures/permissions/legal-ethics/budget claims (the hard rule).
- A `*_review.md` should be cleared (questions answered) before `APPROVED`.

## 5. Hard rules (unchanged in spirit)
- **No fabricated** citation, statistic, scale permission, legal/ethics claim, or
  budget figure may reach `APPROVED`. Agents draft; **humans are accountable**.
- Every change keeps the registries in sync (`PPWS-000-Program-Index.md`,
  `README.md`, `initial_plan.md`) — see PPWS-000C.

## 6. Human roles (credential-bearing)
PI (who may also serve as the owner's academic supervisor, D-0007);
co-investigators (survey / qualitative / analysis); a survey methodologist; a
Pakistani gender scholar; a psychometrician. Org chart and cadence: `PPWS-009`.

## Change log
- 2026-06-06 — Rewrote around autonomous-agent + asynchronous-verification model
  and the review-file convention (D-0008). Status `DRAFT`.
