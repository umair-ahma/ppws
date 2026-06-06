# PPWS-000 — Program Index & Document Registry

> **Status:** Living registry. Update the **Status** column as documents move
> through the lifecycle. This is the master table of contents for the entire
> PPWS document stack (~30 documents). Build order and rationale: see
> [`/initial_plan.md`](../initial_plan.md).

**Status legend:** `NOT STARTED` · `DRAFT` · `IN REVIEW` · `APPROVED` · `FROZEN`
**Source legend:** 🟢 substantially exists in `/source` · 🟡 partially exists · 🔴 net-new

> **Taxonomy note (Decision D-0002):** the ontology now spans **16 domains, A–P**,
> after promoting **Religious & Spiritual Ecology** to its own **Domain J**
> (Workplace→K, Agency→L, Mental→M, Physical→N, Life Satisfaction→O, Future→P).
> The Part-2 ontology file is `…F-P` (renamed from `…F-O`). Binding decisions
> are logged in `00-governance/PPWS-000A-Decision-Log.md`.

---

## Foundation Layer (highest leverage — pure desk work, AI-producible now)
| ID | Document | Path | Depends on | Source | Status |
|---|---|---|---|---|---|
| PPWS-001 | Research Charter (canonical) | `00-governance/PPWS-001-Research-Charter.md` | — | 🟢 | NOT STARTED |
| PPWS-000A | Decision Log | `00-governance/PPWS-000A-Decision-Log.md` | 001 | 🔴 | DRAFT |
| PPWS-000B | Glossary & Unified Domain Taxonomy | `00-governance/PPWS-000B-Glossary-and-Taxonomy.md` | 001, 001A | 🔴 | DRAFT |
| PPWS-000C | Version Control & Doc Governance | `00-governance/PPWS-000C-Version-Control-Protocol.md` | — | 🔴 | NOT STARTED |
| PPWS-000D | AI-Agent + In-House Team Operating Model | `00-governance/PPWS-000D-AI-Agent-Operating-Model.md` | 000C | 🔴 | DRAFT |
| PPWS-001A | Measurement Ontology (master, A–P) | `01-foundation/PPWS-001A-Measurement-Ontology.md` | 001 | 🟡 | DRAFT |
| PPWS-001A-1 | Ontology Part 1 — Domains A–E | `01-foundation/PPWS-001A-1-Ontology-Domains-A-E.md` | 001A | 🟢 | DRAFT |
| PPWS-001A-2 | Ontology Part 2 — Domains F–P (incl. new Religious & Spiritual J) | `01-foundation/PPWS-001A-2-Ontology-Domains-F-P.md` | 001A-1 | 🔴 | DRAFT |
| PPWS-001B | Variable Dictionary | `01-foundation/PPWS-001B-Variable-Dictionary.md` | 001A-2 | 🔴 | NOT STARTED |
| PPWS-001C | Dataset Schema | `01-foundation/PPWS-001C-Dataset-Schema.md` | 001B | 🔴 | NOT STARTED |
| PPWS-001D | Causal Model & SEM Specification | `01-foundation/PPWS-001D-Causal-Model-SEM-Specification.md` | 001A-2, 001B | 🟡 | NOT STARTED |

## Research Layer (what funders score)
| ID | Document | Path | Depends on | Source | Status |
|---|---|---|---|---|---|
| PPWS-002 | Literature Review Framework | `02-research/PPWS-002-Literature-Review-Framework.md` | 001, 001D | 🔴 | DRAFT |
| PPWS-002A | Literature Evidence Matrix | `02-research/PPWS-002A-Literature-Matrix.md` | 002 | 🔴 | NOT STARTED |
| PPWS-003 | Research Methodology | `02-research/PPWS-003-Research-Methodology.md` | 001D, 002 | 🟡 | NOT STARTED |

## Instrument Layer (derived from the ontology)
| ID | Document | Path | Depends on | Source | Status |
|---|---|---|---|---|---|
| PPWS-004 | Questionnaire System (master) | `03-instruments/PPWS-004-Questionnaire-System-Master.md` | 001B, 003 | 🟡 | NOT STARTED |
| PPWS-004A | Demographics (PPWS-D) | `03-instruments/PPWS-004A-Demographics.md` | 004 | 🟡 | NOT STARTED |
| PPWS-004B | Family Ecology Scale (PPWS-F) | `03-instruments/PPWS-004B-Family-Ecology-Scale.md` | 004 | 🟡 | NOT STARTED |
| PPWS-004C | Social Environment Scale (PPWS-S) | `03-instruments/PPWS-004C-Social-Environment-Scale.md` | 004 | 🟡 | NOT STARTED |
| PPWS-004D | Cultural Expectations Scale (PPWS-C) | `03-instruments/PPWS-004D-Cultural-Expectations-Scale.md` | 004 | 🟡 | NOT STARTED |
| PPWS-004E | Workplace Experience Scale (PPWS-W) | `03-instruments/PPWS-004E-Workplace-Experience-Scale.md` | 004 | 🟡 | NOT STARTED |
| PPWS-004F | Agency & Autonomy Scale (PPWS-A) | `03-instruments/PPWS-004F-Agency-Scale.md` | 004 | 🟡 | NOT STARTED |
| PPWS-004G | Mental Wellbeing Scale (PPWS-M) | `03-instruments/PPWS-004G-Mental-Wellbeing-Scale.md` | 004 | 🟡 | NOT STARTED |
| PPWS-004H | Life Satisfaction Scale (PPWS-L) | `03-instruments/PPWS-004H-Life-Satisfaction-Scale.md` | 004 | 🟡 | NOT STARTED |
| PPWS-004I | Future Orientation Scale (PPWS-FO) | `03-instruments/PPWS-004I-Future-Orientation-Scale.md` | 004 | 🟡 | NOT STARTED |
| PPWS-004J | Qualitative Interview Guide | `03-instruments/PPWS-004J-Interview-Guide-Qualitative.md` | 001D, 003 | 🔴 | NOT STARTED |
| PPWS-004K | Validated Scales Register & Permissions | `03-instruments/PPWS-004K-Validated-Scales-Register-and-Permissions.md` | 004 | 🔴 | NOT STARTED |
| PPWS-004L | Translation & Localization Protocol | `03-instruments/PPWS-004L-Translation-Protocol-Urdu-Regional.md` | 004 | 🔴 | NOT STARTED |

## Analytics Layer (de-risk before fieldwork)
| ID | Document | Path | Depends on | Source | Status |
|---|---|---|---|---|---|
| PPWS-005 | Scoring & Interpretation Manual | `04-analytics/PPWS-005-Scoring-and-Interpretation-Manual.md` | 001B, 004 | 🔴 | NOT STARTED |
| PPWS-006 | Synthetic Data Generation Framework | `04-analytics/PPWS-006-Synthetic-Data-Generation-Framework.md` | 001C, 001D | 🟡 | NOT STARTED |
| PPWS-007 | Statistical Analysis Plan (SAP) | `04-analytics/PPWS-007-Statistical-Analysis-Plan.md` | 001D, 006 | 🟡 | NOT STARTED |
| — | Analysis scripts (R) | `04-analytics/analysis/*.R` | 007 | 🔴 | NOT STARTED |
| — | Synthetic data generator (R) | `04-analytics/synthetic-data/generate_synthetic.R` | 006 | 🔴 | NOT STARTED |

## Ethics & Governance Layer (on the critical path — start early)
| ID | Document | Path | Depends on | Source | Status |
|---|---|---|---|---|---|
| PPWS-008 | Ethics & IRB Package | `05-ethics-governance/PPWS-008-Ethics-IRB-Package.md` | 003, 004 | 🟡 | NOT STARTED |
| PPWS-008A | Informed Consent (EN/UR) | `05-ethics-governance/PPWS-008A-Informed-Consent-EN-UR.md` | 008 | 🔴 | NOT STARTED |
| PPWS-008B | Data Management & Protection Plan | `05-ethics-governance/PPWS-008B-Data-Management-and-Protection-Plan.md` | 008 | 🟡 | NOT STARTED |
| PPWS-008C | Data Sharing & Anonymization Protocol | `05-ethics-governance/PPWS-008C-Data-Sharing-and-Anonymization-Protocol.md` | 008B | 🟡 | NOT STARTED |

## Operations Layer
| ID | Document | Path | Depends on | Source | Status |
|---|---|---|---|---|---|
| PPWS-009 | Project Management Plan | `06-operations/PPWS-009-Project-Management-Plan.md` | 001 | 🟡 | NOT STARTED |
| PPWS-009A | Risk Register | `06-operations/PPWS-009A-Risk-Register.md` | 009 | 🟢 | NOT STARTED |
| PPWS-009B | Fieldwork SOP & Sampling Operations | `06-operations/PPWS-009B-Fieldwork-SOP-and-Sampling-Operations.md` | 003, 009 | 🟡 | NOT STARTED |
| PPWS-010 | Budget — Three Costed Tiers (overview) | `06-operations/PPWS-010-Budget-Tiers.md` | 003, 009B | 🟡 | NOT STARTED |
| PPWS-010A | Budget — Pilot/Proof Tier | `06-operations/PPWS-010A-Pilot-Tier-Budget.md` | 010 | 🟡 | NOT STARTED |
| PPWS-010B | Budget — Regional Tier | `06-operations/PPWS-010B-Regional-Tier-Budget.md` | 010 | 🔴 | NOT STARTED |
| PPWS-010C | Budget — National-Ambition Tier | `06-operations/PPWS-010C-National-Tier-Budget.md` | 010 | 🔴 | NOT STARTED |

## Funding Layer (staged — never one big bet)
| ID | Document | Path | Depends on | Source | Status |
|---|---|---|---|---|---|
| PPWS-011 | Funding Strategy | `07-funding/PPWS-011-Funding-Strategy.md` | 010 | 🔴 | NOT STARTED |
| PPWS-011A | Funder Landscape & Target List | `07-funding/PPWS-011A-Funder-Landscape-and-Targets.md` | 011 | 🔴 | NOT STARTED |
| PPWS-011B | Concept Note (5–15 pp) | `07-funding/PPWS-011B-Concept-Note.md` | 011A | 🟡 | NOT STARTED |
| PPWS-011C | Full Grant Proposal Template | `07-funding/PPWS-011C-Full-Proposal-Template.md` | 002, 003, 005, 007, 010 | 🔴 | NOT STARTED |
| PPWS-011D | Institutional Host & PI Plan | `07-funding/PPWS-011D-Institutional-Host-and-PI-Plan.md` | 011 | 🔴 | NOT STARTED |

## Dissemination Layer
| ID | Document | Path | Depends on | Source | Status |
|---|---|---|---|---|---|
| PPWS-012 | Dissemination & Impact Plan | `08-dissemination/PPWS-012-Dissemination-and-Impact-Plan.md` | 007 | 🟡 | NOT STARTED |
| PPWS-012A | Policy Brief Template | `08-dissemination/PPWS-012A-Policy-Brief-Template.md` | 012 | 🔴 | NOT STARTED |
