# Measurement Ontology (Master, Domains A–P)

> **Document ID:** PPWS-001A
> **Layer:** Foundation
> **Status:** `DRAFT`
> **Depends on:** PPWS-001
> **Primary author:** AI research agent  ·  **Human reviewer/sign-off:** TBD (verify-async; see PPWS-000D)
> **Target length / acceptance criteria:** see `../../initial_plan.md`
> **Parts:** `PPWS-001A-1` (Domains A–E) · `PPWS-001A-2` (Domains F–P)
> **Open questions for this document:** `../../ontology_review.md`

## Purpose
The master measurement blueprint: entities, domains, variable classifications,
latent vs observed constructs, mediators, moderators, outcomes, causal
assumptions, boundaries, cohorts, and ontology diagrams. It defines *what reality
the PPWS measures* before any questionnaire item is written. Per **Decision
D-0002** the ontology now spans **16 domains (A–P)** with a dedicated
**Religious & Spiritual Ecology** domain (J).

---

## 1. Scope, entity, and boundaries

- **Unit of analysis (the entity):** an individual **professional woman in
  Pakistan** — age ≥ 25, holding at least a Bachelor's degree, currently employed
  or professionally active (see PPWS-001 §6 Population Definition).
- **What is in scope:** the woman's identity, household and relational ecology,
  professional and economic position, social/cultural/religious environment,
  workplace experience, personal agency, and psychological/physical/life
  outcomes — measured at a **single cross-sectional wave** (D-0004: no
  longitudinal pre-build).
- **What is out of scope (now):** male comparison cohorts, longitudinal panels,
  non-professional women, and multi-language instruments (English-only, D-0003).
- **Time frame:** present-state self-report, with a small number of
  retrospective items (e.g. age at first marriage) and prospective items (future
  orientation).

## 2. Variable classification scheme
Every PPWS variable is tagged on four axes (fully enumerated in PPWS-001B):

1. **Measurement type:** Continuous · Integer/Count · Ordinal (Likert) ·
   Categorical (nominal) · Binary · Text · **Derived index**.
2. **Observability:** **Observed/manifest** (recorded directly) vs **Latent**
   (inferred from multiple indicators via CFA/SEM).
3. **Causal role:** Exogenous control · Predictor · **Mediator** · **Moderator** ·
   **Outcome** · Covariate.
4. **Instrument load:** **CORE** (every respondent) vs **OPTIONAL** (rotating /
   planned-missingness), to hold the core module to ~15–20 minutes.

Coding conventions (shared across all domains): categorical codebook entries for
every nominal variable; reserved missing codes **98 = Not applicable / Not
stated** and **99 = Don't know / Prefer not to answer** (with wider sentinels
`999`/`9999` for numeric fields); negatively worded Likert items reverse-coded so
that **higher = more of the named construct**.

## 3. The 16 domains at a glance

| Domain | Name | Latent construct(s) | Causal role | Primary derived index |
|---|---|---|---|---|
| A | Identity & Demographics | — (mostly manifest) | Exogenous controls | Urbanity, Assets score |
| B | Family Ecology | Family Pressure; Family Support | Predictor/context | Family Support Index, Kinship Support |
| C | Relationship Ecology | Relationship Quality; Spousal Support | Predictor/context | — |
| D | Parenthood Ecology | Parenting Load/Stress | Predictor/load | Care Dependency Index |
| E | Caregiving Ecology | Caregiving Burden | Predictor/load | Caregiving Index |
| F | Professional Ecology | Career Standing | Predictor | Career Complexity, Leadership Responsibility |
| G | Economic Ecology | Economic Independence | Predictor/moderator | Economic Independence Index |
| H | Social Ecology | Social Pressure; Social Support | Predictor/moderator | Social Pressure Index |
| I | Cultural Ecology | Cultural Constraint | Predictor | Cultural Constraint Index |
| **J** | **Religious & Spiritual Ecology** | **Religiosity; Spiritual Wellbeing; Religious Gender-Role Conservatism** | Predictor & **moderator** | **Religiosity Index, Spiritual Wellbeing Index** |
| K | Workplace Ecology | Workplace Equity | Predictor | Workplace Equity Index |
| L | Personal Agency | **Agency / Autonomy** | **Central mediator** | Agency Index |
| M | Mental Wellbeing | Psychological Wellbeing (distress↔resilience) | **Outcome**/mediator | Psychological Wellbeing Index |
| N | Physical Wellbeing | Health Vitality | Outcome/covariate | Health Vitality Index |
| O | Life Satisfaction | Life Satisfaction | **Primary outcome** | Life Satisfaction Index |
| P | Future Orientation | Future Outlook | **Primary outcome** | Future Outlook Index |

## 4. Latent constructs, mediators, moderators, outcomes

- **Central mediator:** **Personal Agency (L)** — the hypothesized hinge through
  which background ecologies (B–E), structural position (F, G, K), and
  environment (H, I, **J**) translate into wellbeing and satisfaction.
- **Primary outcomes:** Life Satisfaction (O), Psychological Wellbeing (M),
  Future Orientation (P), Agency (L, also a mediator), and Professional Success
  (a composite of F + K).
- **Key moderators:** Economic Independence (G), Social Support (H),
  **Religiosity / Spiritual Wellbeing (J)**, marital cohort (A→cohort), and
  caregiving load (D+E). The model explicitly allows religiosity to act **both**
  as a predictor (direct association with wellbeing/identity) **and** as a
  moderator (buffering or amplifying the effect of social/cultural pressure on
  wellbeing).
- **Latent vs observed:** Domains A and most of F/G are largely manifest;
  B (pressure/support), H, I, **J**, L, M, N, O, P are operationalized as
  **latent** constructs with multiple Likert indicators for CFA/SEM.

## 5. Master causal architecture (ordered ecology → mediator → outcome)

```
Identity (A)
   │
Family (B) ─ Relationship (C) ─ Parenthood (D) ─ Caregiving (E)     [household/relational load]
   │
Economic (G) ─ Professional (F) ─ Workplace (K)                      [structural position]
   │
Social (H) ─ Cultural (I) ─ Religious/Spiritual (J)                  [normative environment]
   │
            ▼
     Personal Agency (L)            ◄── central mediator
            │
   ┌────────┼─────────┐
   ▼        ▼         ▼
Mental    Physical   (feeds)
Wellbeing Wellbeing
 (M)        (N)
   │         │
   └────►  Life Satisfaction (O)  ───►  Future Orientation (P)
```

**Reading the diagram:** background and structural ecologies shape the normative
environment a woman experiences; these jointly predict her **Agency**; Agency
drives **Mental** and **Physical** wellbeing, which culminate in **Life
Satisfaction** and **Future Orientation**. **Religiosity/Spiritual (J)** enters
both as a direct predictor of Agency/Wellbeing and as a **moderator** on the
Cultural/Social-pressure → Wellbeing paths. Economic Independence (G) moderates
Family/Cultural pressure → Agency.

> The **confirmatory** models are deliberately *small* (2–4 focused sub-graphs),
> not this full chain estimated at once. Candidate confirmatory hypotheses are
> drafted in `../../ontology_review.md` for the owner to select; the chosen set
> is formalized in `PPWS-001D`.

## 6. Cohorts and weighting hooks
- Cohort assignment derives from **A11 Marital Status** → Cohort A (married) vs
  Cohort B (not currently married).
- Post-stratification weighting variables (D-0001) are carried in Domain A:
  province (A3), urban/rural (A5), age (A1), sector (Domain F), marital cohort.

## 7. Internal-consistency rules (resolved or flagged)
- **NUM_CHILD duplication:** A14 (demographics) and D1 (parenthood) measure the
  same quantity; **A14 is canonical**, D1 is a validation cross-check (resolved in
  PPWS-001B).
- **Religion item vs Domain J:** A7 (Religion, a nominal *affiliation* control)
  is distinct from Domain J constructs (*religiosity, spiritual wellbeing,
  religious gender-role conservatism*). A7 stays in Domain A; J measures
  intensity/meaning, not affiliation.
- **Relationship status** appears as A11 (canonical) and C1 (detailed clarifier);
  C1 must be consistent with A11.

## 8. How downstream documents consume this ontology
`001A` (this master) → `001A-1`/`001A-2` (per-variable specs) → `PPWS-001B`
Variable Dictionary → `PPWS-001C` Dataset Schema → `PPWS-001D` Causal/SEM spec →
`PPWS-004*` instruments → `PPWS-006/007` synthetic data + SAP.

---

## Change log
- 2026-06-06 — Created master; adopted 16-domain A–P taxonomy with new Religious
  & Spiritual Ecology domain (J) per D-0002; documented causal architecture,
  mediators/moderators, and outcomes. Status `DRAFT`. Open items →
  `ontology_review.md`.
