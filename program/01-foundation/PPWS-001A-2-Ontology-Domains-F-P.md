# Ontology Part 2 — Domains F–P (Professional, Economic, Social, Cultural, Religious & Spiritual, Workplace, Agency, Mental, Physical, Life Satisfaction, Future)

> **Document ID:** PPWS-001A-2
> **Layer:** Foundation
> **Status:** `DRAFT`
> **Depends on:** PPWS-001A-1
> **Primary author:** AI research agent  ·  **Human reviewer/sign-off:** TBD (verify-async; see PPWS-000D)
> **Target length / acceptance criteria:** see `../../initial_plan.md`
> **Open questions for this document:** `../../ontology_review.md`

## Purpose
Specifies the remaining domains to the exact depth of Domains A–E (per variable:
type, definition, question stem, response format, validation, missing codes,
derived indices). **Updated per Decision D-0002:** the file now spans **F–P
(11 domains)** and adds a dedicated **Religious & Spiritual Ecology** domain
(**J**), inserted after Cultural Ecology (I). Former J–O (Workplace…Future) shift
to **K–P**.

**Coding conventions (inherited from Part 1):** reserved missing codes
**98 = Not applicable / Not stated**, **99 = Don't know / Prefer not to answer**
(wider numeric sentinels `999`/`9999` where needed); all Likert items are
5-point (1 = Strongly Disagree … 5 = Strongly Agree) unless stated; negatively
worded items are reverse-coded so **higher = more of the named construct**. Each
domain tags its variables CORE/OPTIONAL for instrument-length control (finalized
in PPWS-001B).

---

## Domain F: Professional Ecology

**Purpose:** Define the respondent's workplace position and career structure —
the objective scaffolding of professional life. Charter Domain 2. Mostly manifest
predictors feeding the latent **Career Standing** and the **Professional Success**
outcome.

- **F1. Industry / Sector (INDUSTRY):** *Type:* Categorical. *Definition:* Sector
  of current main employment. *Options:* Health/Medicine [1], Education/Academia
  [2], Engineering/Technology [3], Business/Finance [4], Law [5], Public Sector/
  Civil Service [6], Media/Arts [7], NGO/Development [8], Other [9]. *Question:*
  "Which sector best describes your current main job?" *Response:* Single choice.
  *Use:* Quota + post-stratification stratum (D-0001). *CORE.*
- **F2. Occupation / Role (ROLE):** *Type:* Categorical/Text. *Definition:* Job
  title or role family. *Question:* "What is your current job title or role?"
  *Response:* Coded list or open text. *CORE.*
- **F3. Seniority Level (SENIORITY):** *Type:* Ordinal. *Definition:* Career stage.
  *Options:* Entry [1], Mid [2], Senior [3], Lead/Principal [4], Executive [5].
  *Question:* "Which best describes your seniority level?" *Response:* Single
  choice. *CORE.*
- **F4. Management Level (MGMT_LEVEL):** *Type:* Ordinal. *Definition:* People-
  management scope. *Options:* Individual contributor [0], Team lead [1], Manager
  [2], Senior manager [3], Director+ [4]. *Question:* "Do you manage others, and
  at what level?" *Response:* Single choice. *CORE.*
- **F5. Team Size (TEAM_SIZE):** *Type:* Integer. *Definition:* Number of direct +
  indirect reports. *Question:* "How many people report to you (directly or
  indirectly)?" *Response:* Numeric (0 if none). *OPTIONAL.*
- **F6. Years of Experience (YRS_EXP):** *Type:* Continuous. *Definition:* Total
  years in professional employment. *Question:* "How many years of professional
  work experience do you have in total?" *Response:* Numeric. *Validation:* ≤
  (AGE − 18). *CORE.*
- **F7. Years in Current Position (YRS_POS):** *Type:* Continuous. *Definition:*
  Tenure in current role. *Question:* "How many years have you held your current
  position?" *Response:* Numeric. *OPTIONAL.*
- **F8. Weekly Work Hours (WORK_HOURS):** *Type:* Continuous. *Definition:* Typical
  paid working hours per week. *Question:* "In a typical week, how many hours do
  you work at your paid job?" *Response:* Numeric. *Validation:* If >100,
  re-check. *CORE.*
- **F9. Work Arrangement (REMOTE_STATUS):** *Type:* Categorical. *Definition:*
  Location mode. *Options:* On-site [1], Hybrid [2], Fully remote [3]. *Question:*
  "What is your usual work arrangement?" *Response:* Single choice. *OPTIONAL.*
- **F10. Promotions Count (PROMO_COUNT):** *Type:* Integer. *Definition:* Number of
  promotions received to date. *Question:* "How many promotions have you received
  in your career?" *Response:* Numeric. *OPTIONAL.*
- **F11. Professional Recognition (PROF_RECOG):** *Type:* Ordinal. *Definition:*
  Perceived recognition for one's work. *Question:* "My professional achievements
  are recognized in my field." *Response:* 5-point Likert. *CORE.*
- **F12. Career Satisfaction (CAREER_SAT):** *Type:* Ordinal. *Definition:* Overall
  satisfaction with career trajectory. *Question:* "Overall, how satisfied are you
  with your career so far?" *Response:* 5-point Likert (1 = Very dissatisfied …
  5 = Very satisfied). *CORE.*
- **F13. Career Complexity Index (CAREER_CPLX):** *Type:* Derived. *Definition:*
  Composite of role scope and seniority. *Formula (example):* normalize and sum
  SENIORITY + MGMT_LEVEL + log(1+TEAM_SIZE) + YRS_EXP/10. *Range:* standardized
  z-score. *Use:* indicator of Career Standing latent.
- **F14. Leadership Responsibility Index (LEAD_RESP):** *Type:* Derived.
  *Definition:* People + decision authority. *Formula (example):* MGMT_LEVEL +
  log(1+TEAM_SIZE). *Use:* feeds Professional Success outcome.

*Missing-data & validation:* code 98 for not-applicable (e.g. TEAM_SIZE if
individual contributor → 0, not 98); cross-check YRS_EXP, YRS_POS against AGE.

---

## Domain G: Economic Ecology

**Purpose:** Quantify economic power and independence — a key **moderator** of
pressure→agency paths. Charter Domain 3. Note some items overlap with Domain A
(A16–A19); Domain G is the **analytic home** for the Economic Independence
latent; A-items are demographic controls (reconciled in PPWS-001B).

- **G1. Personal Monthly Income (PERS_INC_G):** *Type:* Categorical/Continuous.
  *Definition:* Respondent's own income (cross-ref A17). *Question:* "What is your
  own total monthly income from all sources (PKR)?" *Response:* Brackets or
  numeric. *Missing:* 98 = Prefer not to say. *CORE.*
- **G2. Income Share of Household (INC_SHARE):** *Type:* Ordinal. *Definition:*
  Respondent's contribution to household income. *Options:* None [0], <25% [1],
  25–50% [2], ~50% [3], >50% [4], Sole earner [5]. *Question:* "Roughly what share
  of your household's income do you personally provide?" *Response:* Single
  choice. *CORE.*
- **G3. Asset Ownership (ASSETS_G):** *Type:* Index (derived). *Definition:* Count
  of durable/financial assets personally or jointly owned (car, property, savings,
  investments, gold). *Question:* "Which of the following do you own (alone or
  jointly)?" *Response:* Multi-check. *Use:* cross-ref A19. *OPTIONAL.*
- **G4. Savings Adequacy (SAVINGS):** *Type:* Ordinal. *Definition:* Perceived
  savings buffer. *Question:* "If income stopped, my savings could cover my
  expenses for…" *Options:* <1 month [1], 1–3 [2], 3–6 [3], 6–12 [4], >12 [5].
  *Response:* Single choice. *OPTIONAL.*
- **G5. Debt Burden (DEBT):** *Type:* Ordinal. *Definition:* Subjective debt
  pressure. *Question:* "Debt or loan repayments are a burden on me." *Response:*
  5-point Likert. *OPTIONAL.*
- **G6. Financial Autonomy (FIN_AUTO):** *Type:* Ordinal. *Definition:* Freedom to
  make major purchases/financial decisions without permission. *Question:* "I can
  make major financial decisions (large purchases, investments) on my own."
  *Response:* 5-point Likert. *CORE.* *Note:* shares variance with Agency (L) but
  measured here as an economic capability indicator.
- **G7. Financial Literacy (FIN_LIT):** *Type:* Ordinal/Index. *Definition:*
  Self-rated or short-quiz financial knowledge. *Question:* "How would you rate
  your understanding of budgeting, saving, and investing?" *Response:* 5-point
  (Very low … Very high). *OPTIONAL.*
- **G8. Home Ownership (HOMEOWN_G):** *Type:* Binary. *Definition:* Owns/jointly
  owns residence (cross-ref A18). *Question:* "Do you own (alone or jointly) the
  home you live in?" *Response:* Yes=1/No=0. *OPTIONAL.*
- **G9. Economic Independence Index (ECON_INDEP):** *Type:* Derived. *Definition:*
  The Domain-G latent's summary score. *Formula (example):* standardized mean of
  PERS_INC_G, INC_SHARE, FIN_AUTO, SAVINGS, ASSETS_G. *Range:* 0–100 normalized.
  *Use:* **primary moderator** in confirmatory models; controls in others.

*Missing-data & validation:* income items allow 98 (prefer not to say);
reconcile G1↔A17, G3↔A19, G8↔A18 in the dictionary (Domain G is canonical for the
economic latent).

---

## Domain H: Social Ecology

**Purpose:** Capture the proximal social environment — pressure, judgement, and
support from community and networks. Charter Domain 8. Two latents: **Social
Pressure** and **Social Support**.

- **H1. Community Acceptance (COMM_ACCEPT):** *Type:* Ordinal. *Definition:* Felt
  acceptance by one's community as a professional woman. *Question:* "My community
  accepts and respects my choices as a working woman." *Response:* 5-point Likert.
  *CORE.*
- **H2. Marriage Expectation Pressure (MARR_PRESS_H):** *Type:* Ordinal.
  *Definition:* Social (non-family) pressure regarding marriage/timing. *Question:*
  "People in my social circle pressure me about getting married or my marital
  status." *Response:* 5-point Likert. *CORE.*
- **H3. Reputation / Gossip Concern (REPUTATION):** *Type:* Ordinal. *Definition:*
  Concern about gossip or social judgement. *Question:* "I worry about being
  judged or talked about because of my life choices." *Response:* 5-point Likert.
  *CORE.*
- **H4. Perceived Social Stigma (STIGMA):** *Type:* Ordinal. *Definition:* Felt
  stigma for status (e.g. unmarried, divorced, career-focused). *Question:* "I
  have felt stigmatized because of my marital status or career." *Response:*
  5-point Likert. *CORE.*
- **H5. Social Support Network (SOC_SUPPORT):** *Type:* Ordinal. *Definition:*
  Availability of supportive friends/peers. *Question:* "I have friends or peers I
  can rely on for emotional support." *Response:* 5-point Likert. *CORE.*
- **H6. Social Participation (SOC_PARTIC):** *Type:* Ordinal. *Definition:*
  Involvement in social/community/professional groups. *Question:* "I actively
  participate in social, community, or professional groups." *Response:* 5-point
  Likert (Never … Very often). *OPTIONAL.*
- **H7. Social Isolation (ISOLATION):** *Type:* Ordinal (reverse-coded).
  *Definition:* Felt loneliness/isolation. *Question:* "I often feel socially
  isolated or lonely." *Response:* 5-point Likert (reverse-coded into support).
  *OPTIONAL.*
- **H8. Social Pressure Index (SOC_PRESS_IDX):** *Type:* Derived. *Definition:*
  Summary of normative social pressure. *Formula (example):* mean of
  MARR_PRESS_H, REPUTATION, STIGMA (H1, H5, H7 form the inverse Support side).
  *Use:* predictor; interacts with Religiosity (J) and Economic Independence (G).
- **H9. Social Support Index (SOC_SUPP_IDX):** *Type:* Derived. *Definition:*
  Summary of available support. *Formula (example):* mean of SOC_SUPPORT,
  COMM_ACCEPT, SOC_PARTIC, reverse(ISOLATION). *Use:* **buffering moderator**.

*Missing-data & validation:* standard 98/99; H4/H7 are negatively framed —
reverse-code consistently.

---

## Domain I: Cultural Ecology

**Purpose:** Measure exposure to and internalization of traditional gender/cultural
norms. Charter Domain 9. Latent: **Cultural Constraint**.

- **I1. Traditional Gender Expectations (TRAD_GENDER):** *Type:* Ordinal.
  *Definition:* Perceived expectation to conform to traditional female roles.
  *Question:* "I am expected to prioritize traditional female roles (home, family)
  over my career." *Response:* 5-point Likert. *CORE.*
- **I2. Family Honor Expectation (HONOR_EXP):** *Type:* Ordinal. *Definition:*
  Pressure to protect family honor through one's conduct. *Question:* "My behavior
  is expected to protect my family's honor and reputation." *Response:* 5-point
  Likert. *CORE.*
- **I3. Domestic Role Expectation (DOMESTIC_EXP):** *Type:* Ordinal. *Definition:*
  Expectation to perform domestic duties regardless of employment. *Question:*
  "Regardless of my job, I am expected to handle most household duties."
  *Response:* 5-point Likert. *CORE.*
- **I4. Community Conformity Pressure (CONFORMITY):** *Type:* Ordinal.
  *Definition:* Pressure to conform to community norms. *Question:* "I feel
  pressure to conform to what my community considers proper for a woman."
  *Response:* 5-point Likert. *CORE.*
- **I5. Mobility Restriction (MOBILITY_NORM):** *Type:* Ordinal. *Definition:*
  Cultural limits on free movement/travel. *Question:* "There are restrictions on
  where I can go or travel alone." *Response:* 5-point Likert. *OPTIONAL.*
- **I6. Cultural Value of Women's Career (CAREER_VALUE):** *Type:* Ordinal
  (reverse-coded). *Definition:* Perceived cultural endorsement of women's
  careers. *Question:* "In my culture, a woman's education and career are valued."
  *Response:* 5-point Likert (reverse into constraint). *OPTIONAL.*
- **I7. Taboo Sensitivity (TABOO):** *Type:* Ordinal. *Definition:* Constraint from
  taboos on women's behavior (dress, socializing). *Question:* "There are many
  things I cannot do publicly because they are considered improper for a woman."
  *Response:* 5-point Likert. *OPTIONAL.*
- **I8. Cultural Constraint Index (CULT_CONSTRAINT):** *Type:* Derived.
  *Definition:* Summary of cultural constraint. *Formula (example):* mean of
  TRAD_GENDER, HONOR_EXP, DOMESTIC_EXP, CONFORMITY, MOBILITY_NORM, TABOO,
  reverse(CAREER_VALUE). *Use:* predictor of Agency; **moderated by Religiosity
  (J)**.

*Missing-data & validation:* 98/99; I6 reverse-coded. Cultural and religious
constraint are correlated but distinct — see Domain J boundary note.

---

## Domain J: Religious & Spiritual Ecology  *(NEW — Decision D-0002)*

**Purpose:** Capture **religiosity, spirituality, and religious gender-role
conservatism** as discrete, measurable constructs — distinct from nominal
religious *affiliation* (A7) and from general *cultural* constraint (Domain I).
Charter Domain 10. This domain exists because (a) spirituality is a major driver
of life satisfaction in this population, (b) religion is inseparable from identity
and partner-matching in the Pakistani context, and (c) keeping it as a discrete
latent lets it function as **both a predictor and a moderator** in the SEM.
Latents: **Religiosity (behavioral + intrinsic)**, **Spiritual Wellbeing**, and
**Religious Gender-Role Conservatism**. Wherever possible, items map to validated
scales (e.g. Centrality of Religiosity Scale, intrinsic/extrinsic religiosity,
spiritual wellbeing scales) — see PPWS-004K for the scales register and
permissions.

**Boundary rules:** A7 (affiliation) and A20 (caste/clan) stay in Domain A.
Domain J measures *intensity, meaning, and gendered religious belief*, never
affiliation. Items are phrased to be **denomination-neutral** (applicable to any
faith) and are **OPTIONAL/sensitive** unless marked CORE.

### J.1 Religiosity (behavioral & intrinsic)
- **J1. Religious Affiliation Strength (REL_STRENGTH):** *Type:* Ordinal.
  *Definition:* Self-rated importance of religion in life. *Question:* "How
  important is religion in your daily life?" *Response:* 5-point (Not at all …
  Extremely). *CORE.*
- **J2. Religious Practice Frequency (REL_PRACTICE):** *Type:* Ordinal.
  *Definition:* Frequency of personal religious practice (prayer, worship,
  reading). *Question:* "How often do you engage in personal religious practices
  (prayer, worship, scripture)?" *Options:* Never [1], Rarely [2], Weekly [3],
  Daily [4], Multiple times daily [5]. *Response:* Single choice. *CORE.*
- **J3. Communal Religious Participation (REL_COMMUNAL):** *Type:* Ordinal.
  *Definition:* Participation in communal/organized religious activity.
  *Question:* "How often do you take part in communal religious gatherings or
  events?" *Response:* 5-point frequency. *OPTIONAL.*
- **J4. Intrinsic Religiosity (REL_INTRINSIC):** *Type:* Ordinal. *Definition:*
  Religion as an internalized, guiding framework (vs social conformity).
  *Question:* "My religious beliefs guide my approach to my whole life."
  *Response:* 5-point Likert. *CORE.*
- **J5. Religious Coping (REL_COPING):** *Type:* Ordinal. *Definition:* Use of
  faith to cope with stress/adversity. *Question:* "When facing difficulties, I
  draw strength from my faith." *Response:* 5-point Likert. *CORE.* *Use:*
  candidate **moderator** on stress→wellbeing paths.

### J.2 Spiritual wellbeing
- **J6. Sense of Meaning/Purpose (SPIRIT_MEANING):** *Type:* Ordinal. *Definition:*
  Spiritually grounded sense of meaning. *Question:* "My spiritual or religious
  life gives me a sense of meaning and purpose." *Response:* 5-point Likert.
  *CORE.*
- **J7. Inner Peace (SPIRIT_PEACE):** *Type:* Ordinal. *Definition:* Felt
  spiritual peace/contentment. *Question:* "My faith gives me a feeling of inner
  peace." *Response:* 5-point Likert. *OPTIONAL.*
- **J8. Spiritual Connection (SPIRIT_CONNECT):** *Type:* Ordinal. *Definition:*
  Felt connection to the transcendent/God. *Question:* "I feel a strong personal
  connection with the divine." *Response:* 5-point Likert. *OPTIONAL.*

### J.3 Religious gender-role conservatism & autonomy tension
- **J9. Religious Gender-Role Conservatism (REL_GENDER_CONS):** *Type:* Ordinal.
  *Definition:* Endorsement of traditional, religiously framed gender roles.
  *Question:* "I believe a woman's primary religious duty is to her home and
  family before her career." *Response:* 5-point Likert. *CORE.* *Note:* distinct
  from cultural norm (I) — this is the *religiously justified* belief.
- **J10. Family Religious Conservatism (FAM_REL_CONS):** *Type:* Ordinal.
  *Definition:* Conservatism of the respondent's family/household on religious
  matters. *Question:* "My family interprets religion in a strict or conservative
  way." *Response:* 5-point Likert. *CORE.*
- **J11. Personal–Familial Religious Tension (REL_TENSION):** *Type:* Ordinal.
  *Definition:* Conflict between own and family's religious expectations.
  *Question:* "My own religious views differ from what my family expects of me."
  *Response:* 5-point Likert. *OPTIONAL.* *Use:* candidate predictor of
  distress/agency tension.
- **J12. Religious Justification of Constraints (REL_CONSTRAINT):** *Type:*
  Ordinal. *Definition:* Degree to which restrictions on the respondent are
  justified to her on religious grounds. *Question:* "Restrictions on my choices
  are often explained to me as religious requirements." *Response:* 5-point
  Likert. *OPTIONAL.*

### J.4 Partner / matching relevance (identity)
- **J13. Religious Compatibility Priority (REL_MATCH):** *Type:* Ordinal.
  *Definition:* Importance of shared religiosity in a (potential) partner —
  reflects the identity/matching salience the owner highlighted. *Question:* "A
  shared level of religious commitment is important to me in a spouse or partner."
  *Response:* 5-point Likert. *OPTIONAL.*

### J.5 Derived indices
- **J14. Religiosity Index (RELIGIOSITY_IDX):** *Type:* Derived. *Definition:*
  Composite of behavioral + intrinsic religiosity. *Formula (example):*
  standardized mean of REL_STRENGTH, REL_PRACTICE, REL_INTRINSIC, REL_COPING,
  REL_COMMUNAL. *Range:* 0–100 normalized. *Use:* **predictor and moderator**.
- **J15. Spiritual Wellbeing Index (SPIRIT_WB_IDX):** *Type:* Derived.
  *Definition:* Composite spiritual wellbeing. *Formula (example):* mean of
  SPIRIT_MEANING, SPIRIT_PEACE, SPIRIT_CONNECT. *Use:* predictor of Life
  Satisfaction (O) and Mental Wellbeing (M).
- **J16. Religious Conservatism Index (REL_CONS_IDX):** *Type:* Derived.
  *Definition:* Gendered religious conservatism. *Formula (example):* mean of
  REL_GENDER_CONS, FAM_REL_CONS, REL_CONSTRAINT. *Use:* predictor of Cultural
  Constraint and **moderator** of pressure→agency.

*Measurement & ethics notes:* religion items are sensitive; all carry an explicit
"prefer not to answer" (99) and are skippable. Phrasing is denomination-neutral
so the domain is valid across faiths represented in A7. Validated-scale sourcing
and permissions are tracked in PPWS-004K. Open design questions (e.g. whether to
administer a short validated religiosity scale verbatim vs adapted items) are
logged in `../../ontology_review.md`.

---

## Domain K: Workplace Ecology  *(was J)*

**Purpose:** Measure organizational experience and equity. Charter Domain 11.
Latent: **Workplace Equity**.

- **K1. Promotion Fairness (PROMO_FAIR):** *Type:* Ordinal. *Definition:* Perceived
  fairness of advancement. *Question:* "Promotions in my workplace are awarded
  fairly regardless of gender." *Response:* 5-point Likert. *CORE.*
- **K2. Workplace Inclusion (INCLUSION):** *Type:* Ordinal. *Definition:* Felt
  inclusion in teams/decisions. *Question:* "I feel included in important decisions
  and networks at work." *Response:* 5-point Likert. *CORE.*
- **K3. Leadership Access (LEAD_ACCESS):** *Type:* Ordinal. *Definition:* Access to
  leadership/advancement opportunities. *Question:* "I have the same access to
  leadership opportunities as my male colleagues." *Response:* 5-point Likert.
  *CORE.*
- **K4. Gender Bias Experience (BIAS_EXP):** *Type:* Ordinal. *Definition:*
  Frequency of experienced gender bias/discrimination. *Question:* "I have
  experienced bias or discrimination at work because I am a woman." *Response:*
  5-point Likert (Never … Very often). *CORE.*
- **K5. Discriminatory Comments (DISCRIM_COMMENT):** *Type:* Ordinal. *Definition:*
  Exposure to demeaning comments. *Question:* "I have been subjected to demeaning
  or inappropriate comments at work." *Response:* 5-point frequency. *OPTIONAL.*
- **K6. Mentorship Access (MENTORSHIP):** *Type:* Ordinal. *Definition:*
  Availability of mentors/sponsors. *Question:* "I have access to mentors who
  support my career growth." *Response:* 5-point Likert. *OPTIONAL.*
- **K7. Employer Flexibility (FLEXIBILITY):** *Type:* Ordinal. *Definition:*
  Supportive policies (leave, scheduling). *Question:* "My employer offers
  flexibility (maternity leave, scheduling) that supports my life." *Response:*
  5-point Likert. *OPTIONAL.*
- **K8. Job Security (JOB_SECURITY):** *Type:* Ordinal. *Definition:* Perceived
  security of employment. *Question:* "I feel secure in my job." *Response:*
  5-point Likert. *OPTIONAL.*
- **K9. Workplace Equity Index (WORK_EQUITY):** *Type:* Derived. *Definition:*
  Summary equity score. *Formula (example):* mean of PROMO_FAIR, INCLUSION,
  LEAD_ACCESS, MENTORSHIP, FLEXIBILITY, reverse(BIAS_EXP), reverse(DISCRIM_COMMENT).
  *Use:* predictor; component of Professional Success outcome.

*Missing-data & validation:* 98 if not currently employed (route around); K4/K5
negatively framed → reverse-code.

---

## Domain L: Personal Agency  *(was K) — CENTRAL MEDIATOR*

**Purpose:** Measure the respondent's perceived ability to control and direct her
own life — the **central mediator** of the causal model. Charter Domain 12.
Latent: **Agency / Autonomy**. Maps to validated autonomy/self-determination
scales (PPWS-004F, 004K).

- **L1. Decision Autonomy (DECISION_AUTO):** *Type:* Ordinal. *Definition:* Control
  over everyday and major personal decisions. *Question:* "I make my own decisions
  about important matters in my life." *Response:* 5-point Likert. *CORE.*
- **L2. Financial Autonomy (FIN_AUTO_L):** *Type:* Ordinal. *Definition:* Control
  over personal finances (analytic link to G6). *Question:* "I control how my own
  money is spent." *Response:* 5-point Likert. *CORE.*
- **L3. Mobility Autonomy (MOBILITY_AUTO):** *Type:* Ordinal. *Definition:* Freedom
  to move/travel as needed. *Question:* "I can travel where I need to without
  seeking permission." *Response:* 5-point Likert. *CORE.*
- **L4. Career Autonomy (CAREER_AUTO):** *Type:* Ordinal. *Definition:* Control
  over career choices. *Question:* "I am free to make my own career choices."
  *Response:* 5-point Likert. *CORE.*
- **L5. Relationship Autonomy (REL_AUTO):** *Type:* Ordinal. *Definition:* Control
  over relationship/marriage decisions. *Question:* "I have control over decisions
  about my relationships or marriage." *Response:* 5-point Likert. *CORE.*
- **L6. Self-Determination (SELF_DETERMINE):** *Type:* Ordinal. *Definition:*
  General sense of running one's own life. *Question:* "I feel in control of the
  direction of my life." *Response:* 5-point Likert. *CORE.*
- **L7. Goal-Setting Confidence (GOAL_CONF):** *Type:* Ordinal. *Definition:*
  Confidence to set and pursue personal goals. *Question:* "I am confident in
  setting and pursuing my own goals." *Response:* 5-point Likert. *OPTIONAL.*
- **L8. Agency Index (AGENCY_IDX):** *Type:* Derived. *Definition:* Summary agency
  score (the mediator). *Formula (example):* standardized mean of L1–L7. *Range:*
  0–100 normalized. *Use:* **central mediator** in all confirmatory models.

*Missing-data & validation:* 98 if item not applicable (e.g. REL_AUTO if the
respondent reports it irrelevant); all items positively framed.

---

## Domain M: Mental Wellbeing  *(was L) — PRIMARY OUTCOME*

**Purpose:** Measure psychological distress and resilience — a **primary
outcome** and partial mediator. Charter Domain 13. Maps to **DASS-21**,
**Rosenberg Self-Esteem**, **CD-RISC** (resilience) where licensing permits
(PPWS-004G, 004K). Latent: **Psychological Wellbeing** (distress ↔ resilience).

- **M1. Stress (STRESS):** *Type:* Ordinal. *Definition:* Recent perceived stress.
  *Question:* "Over the past two weeks, I felt stressed or unable to cope."
  *Response:* 5-point frequency. *CORE.*
- **M2. Anxiety (ANXIETY):** *Type:* Ordinal. *Definition:* Recent anxiety
  symptoms. *Question:* "Over the past two weeks, I felt anxious or on edge."
  *Response:* 5-point frequency. *CORE.*
- **M3. Depressive Symptoms (DEPRESSION):** *Type:* Ordinal. *Definition:* Recent
  low mood/anhedonia. *Question:* "Over the past two weeks, I felt down,
  depressed, or hopeless." *Response:* 5-point frequency. *CORE.*
- **M4. Emotional Exhaustion / Burnout (BURNOUT):** *Type:* Ordinal. *Definition:*
  Felt depletion from roles. *Question:* "I feel emotionally drained by my daily
  responsibilities." *Response:* 5-point Likert. *CORE.*
- **M5. Self-Esteem (SELF_ESTEEM):** *Type:* Ordinal. *Definition:* Global
  self-worth. *Question:* "On the whole, I am satisfied with myself." *Response:*
  5-point Likert. *CORE.*
- **M6. Resilience (RESILIENCE):** *Type:* Ordinal. *Definition:* Capacity to
  recover from adversity. *Question:* "I bounce back quickly after hard times."
  *Response:* 5-point Likert. *CORE.*
- **M7. Guilt/Shame from Pressure (GUILT):** *Type:* Ordinal. *Definition:*
  Pressure-linked guilt/shame. *Question:* "I feel guilty or ashamed for not
  meeting others' expectations of me." *Response:* 5-point Likert. *OPTIONAL.*
- **M8. Psychological Wellbeing Index (PSYCH_WB):** *Type:* Derived. *Definition:*
  Summary wellbeing (high = better). *Formula (example):* standardized mean of
  reverse(STRESS, ANXIETY, DEPRESSION, BURNOUT, GUILT) + SELF_ESTEEM + RESILIENCE.
  *Range:* 0–100 normalized. *Use:* **primary outcome**; mediates Agency→Life
  Satisfaction.

*Missing-data & validation:* clinical-style items carry signposting to support
resources in the instrument (ethics, PPWS-008); distress items reverse-coded into
wellbeing.

---

## Domain N: Physical Wellbeing  *(was M)*

**Purpose:** Measure self-reported physical health and vitality — outcome and
covariate. Charter Domain 14. Latent: **Health Vitality**.

- **N1. Self-Rated Health (HEALTH_SELF):** *Type:* Ordinal. *Definition:* Global
  health rating. *Question:* "In general, how would you rate your health?"
  *Options:* Poor [1] … Excellent [5]. *Response:* Single choice. *CORE.*
- **N2. Sleep Quality (SLEEP):** *Type:* Ordinal. *Definition:* Typical sleep
  quality. *Question:* "How would you rate the quality of your sleep?" *Response:*
  5-point (Very poor … Very good). *CORE.*
- **N3. Fatigue (FATIGUE):** *Type:* Ordinal. *Definition:* Frequency of fatigue/
  low energy. *Question:* "I often feel physically tired or low on energy."
  *Response:* 5-point frequency. *CORE.*
- **N4. Chronic Conditions (CHRONIC):** *Type:* Binary/Count. *Definition:* Presence
  of diagnosed chronic conditions. *Question:* "Do you have any long-term/chronic
  health conditions? If yes, how many?" *Response:* Yes=1/No=0 (+count).
  *OPTIONAL.*
- **N5. Physical Activity (EXERCISE):** *Type:* Ordinal. *Definition:* Frequency of
  exercise. *Question:* "How often do you engage in physical exercise?"
  *Response:* 5-point frequency. *OPTIONAL.*
- **N6. Nutrition (NUTRITION):** *Type:* Ordinal. *Definition:* Perceived diet
  quality. *Question:* "I am able to eat a healthy, balanced diet." *Response:*
  5-point Likert. *OPTIONAL.*
- **N7. Body Image Satisfaction (BODY_IMAGE):** *Type:* Ordinal. *Definition:*
  Satisfaction with one's body. *Question:* "I am satisfied with my physical
  appearance." *Response:* 5-point Likert. *OPTIONAL.*
- **N8. Health Vitality Index (HEALTH_VITALITY):** *Type:* Derived. *Definition:*
  Summary physical wellbeing. *Formula (example):* standardized mean of
  HEALTH_SELF, SLEEP, reverse(FATIGUE), EXERCISE, NUTRITION, reverse(CHRONIC).
  *Range:* 0–100 normalized. *Use:* outcome/covariate for Life Satisfaction.

*Missing-data & validation:* 98/99; N3 reverse-coded; CHRONIC count validated ≥0.

---

## Domain O: Life Satisfaction  *(was N) — PRIMARY OUTCOME*

**Purpose:** Measure global life satisfaction and fulfillment — a **primary
distal outcome**. Charter Domain 15 (part). Maps to **SWLS** (adapted; PPWS-004H,
004K). Latent: **Life Satisfaction**.

- **O1. Overall Life Satisfaction (LIFE_SAT):** *Type:* Ordinal. *Definition:*
  Global satisfaction. *Question:* "In most ways my life is close to my ideal."
  *Response:* 5-point Likert (SWLS-style). *CORE.*
- **O2. Conditions of Life (LIFE_COND):** *Type:* Ordinal. *Definition:*
  Satisfaction with life conditions. *Question:* "The conditions of my life are
  excellent." *Response:* 5-point Likert. *CORE.*
- **O3. Satisfaction with Achievements (ACHIEVE_SAT):** *Type:* Ordinal.
  *Definition:* Satisfaction with what one has achieved. *Question:* "So far I have
  gotten the important things I want in life." *Response:* 5-point Likert. *CORE.*
- **O4. Happiness (HAPPINESS):** *Type:* Ordinal. *Definition:* General happiness.
  *Question:* "Taking all things together, I would say I am happy." *Response:*
  5-point Likert. *CORE.*
- **O5. Sense of Fulfillment (FULFILLMENT):** *Type:* Ordinal. *Definition:* Felt
  fulfillment/meaning in life. *Question:* "My life feels meaningful and
  fulfilling." *Response:* 5-point Likert. *CORE.*
- **O6. Would Change Nothing (LIFE_NOCHANGE):** *Type:* Ordinal. *Definition:* SWLS
  closing item. *Question:* "If I could live my life over, I would change almost
  nothing." *Response:* 5-point Likert. *OPTIONAL.*
- **O7. Life Satisfaction Index (LIFE_SAT_IDX):** *Type:* Derived. *Definition:*
  Summary satisfaction. *Formula (example):* standardized mean of O1–O6. *Range:*
  0–100 normalized. *Use:* **primary outcome** (ultimate dependent variable).

*Missing-data & validation:* 99 only; all positively framed (SWLS convention).

---

## Domain P: Future Orientation  *(was O) — PRIMARY OUTCOME*

**Purpose:** Measure optimism and forward-looking confidence/goals — a **primary
distal outcome**. Charter Domain 15 (part). Latent: **Future Outlook**.

- **P1. Optimism (OPTIMISM):** *Type:* Ordinal. *Definition:* General optimism
  about the future. *Question:* "I am optimistic about my future." *Response:*
  5-point Likert. *CORE.*
- **P2. Future Confidence (FUTURE_CONF):** *Type:* Ordinal. *Definition:*
  Confidence in achieving a good future. *Question:* "I am confident I can build
  the future I want." *Response:* 5-point Likert. *CORE.*
- **P3. Perceived Control over Future (FUTURE_CONTROL):** *Type:* Ordinal.
  *Definition:* Sense of control over what comes next. *Question:* "I have control
  over how my future turns out." *Response:* 5-point Likert. *CORE.*
- **P4. Career Goals (CAREER_GOALS):** *Type:* Ordinal. *Definition:* Clarity/
  strength of career aspirations. *Question:* "I have clear goals for my career."
  *Response:* 5-point Likert. *OPTIONAL.*
- **P5. Family/Personal Goals (FAMILY_GOALS):** *Type:* Ordinal. *Definition:*
  Clarity of personal/family aspirations. *Question:* "I have clear goals for my
  personal and family life." *Response:* 5-point Likert. *OPTIONAL.*
- **P6. Hope/Agency for Goals (HOPE):** *Type:* Ordinal. *Definition:* Belief in
  pathways to goals. *Question:* "I can think of many ways to reach my goals."
  *Response:* 5-point Likert. *OPTIONAL.*
- **P7. Future Outlook Index (FUTURE_OUTLOOK):** *Type:* Derived. *Definition:*
  Summary future orientation. *Formula (example):* standardized mean of P1–P6.
  *Range:* 0–100 normalized. *Use:* **primary outcome**.

*Missing-data & validation:* 99 only; all positively framed.

---

## Cross-domain notes
- **Index normalization:** all derived indices in this part are illustrative
  ("Formula (example)"); the **authoritative** formulas, ranges, and CORE/OPTIONAL
  tags are finalized in **PPWS-001B Variable Dictionary** and operationalized in
  **PPWS-001C Dataset Schema**.
- **Reconciliations to resolve in PPWS-001B:** G1↔A17, G3↔A19, G8↔A18 (economic);
  L2↔G6 (financial autonomy appears as both an economic capability and an agency
  indicator — keep both, flag shared variance); A7 (affiliation) vs Domain J
  (religiosity/spirituality).
- **Validated-scale mapping** (DASS-21, SWLS, Rosenberg, CD-RISC, religiosity/
  spiritual-wellbeing scales, autonomy scales) and **permissions** are tracked in
  **PPWS-004K**.

## Change log
- 2026-06-06 — Authored F–P to A–E depth; **added Domain J Religious & Spiritual
  Ecology** and shifted Workplace→K, Agency→L, Mental→M, Physical→N, Life
  Satisfaction→O, Future→P (D-0002). File renamed `…F-O` → `…F-P`. Status `DRAFT`.
  Open items → `ontology_review.md`.
