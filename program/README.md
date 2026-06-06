# PPWS Program — Research Operating System

This `program/` folder is the **research operating system** for the Pakistan
Professional Women Study (PPWS): the complete, pre-allocated document stack that
turns the blueprint corpus in `/source` into a funded, executable national
research program.

> Every file here is currently an **allocated placeholder** (`NOT STARTED`).
> The build sequence, dependency order, ownership model, and acceptance
> criteria are defined in the root **[`/initial_plan.md`](../initial_plan.md)**.
> The live registry of all documents and their status is
> **[`PPWS-000-Program-Index.md`](PPWS-000-Program-Index.md)**.

## Why this structure
The PPWS corpus is not a codebase — it is the founding document set of a
research institute-in-waiting. The governing discipline is **ontology-first**:

```
Charter → Measurement Ontology → Variable Dictionary → Dataset Schema →
Causal Model → Research Questions → Questionnaires → Statistical Models
```

Define *the reality to be measured* before writing questions. Once the
Foundation Layer (`01-foundation`) exists, almost everything downstream becomes
mechanical and largely AI-producible.

## Folder map
| Folder | Layer | Contents |
|---|---|---|
| `00-governance/` | Governance | Canonical charter, decision log, taxonomy, version control, **AI-agent operating model** |
| `01-foundation/` | Foundation | Measurement ontology (A–O), variable dictionary, dataset schema, causal/SEM model |
| `02-research/` | Research | Literature review framework + matrix, research methodology |
| `03-instruments/` | Instrument | Questionnaire system, 9 scale modules, interview guide, scales register, translation protocol |
| `04-analytics/` | Analytics | Scoring manual, synthetic-data framework, SAP + reproducible `analysis/` and `synthetic-data/` scripts |
| `05-ethics-governance/` | Ethics | IRB package, consent forms, data management/protection, anonymization |
| `06-operations/` | Operations | Project plan, risk register, fieldwork SOP, **three-tier budget** |
| `07-funding/` | Funding | Funding strategy, funder landscape, concept note, full-proposal template, PI/host plan |
| `08-dissemination/` | Dissemination | Dissemination & impact plan, policy-brief template |

## Document ID convention
`PPWS-<NNN><optional letter>-<Short-Title>.md` — e.g. `PPWS-001A-Measurement-Ontology.md`.
Numbers encode build order; letters encode parts/children of a parent document.

## Status lifecycle
`NOT STARTED → DRAFT → IN REVIEW → APPROVED → FROZEN`
(see `00-governance/PPWS-000C-Version-Control-Protocol.md`).
