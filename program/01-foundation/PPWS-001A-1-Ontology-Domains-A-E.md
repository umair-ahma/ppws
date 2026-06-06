# Ontology Part 1 — Domains A–E (Identity, Family, Relationship, Parenthood, Caregiving)

> **Document ID:** PPWS-001A-1
> **Layer:** Foundation
> **Status:** `DRAFT`
> **Depends on:** PPWS-001A
> **Primary author:** AI research agent (migrated from source charter)  ·  **Human reviewer/sign-off:** TBD (verify-async; see PPWS-000D)
> **Target length / acceptance criteria:** see `../../initial_plan.md`
> **Provenance:** Migrated verbatim from `source/PPWS-001-Research-Charter.md` (Measurement Ontology Part 1) and brought under version control as the **reference quality bar** for Part 2 (F–P).

## Purpose
The existing, publishable-standard portion of the ontology (~60 variables across
Domains A–E). Domains F–P replicate this depth and format in `PPWS-001A-2`.

> **Taxonomy note (D-0002):** A–E are unchanged by the Religious-domain decision;
> the new **Religious & Spiritual Ecology** domain is **J** in Part 2. Domain A
> retains **A7 Religion** as a nominal *affiliation* control, which is distinct
> from the *religiosity/spirituality* constructs in Domain J.

---

## Domain A: Identity and Demographics

**Purpose:** To capture fundamental personal and situational attributes of each participant. These are primarily control variables and are mostly exogenous in causal models.

- **A1. Age (AGE):** *Type:* Continuous integer (years). *Definition:* Respondent’s age at last birthday. *Question:* “What is your age (in years)?” *Response:* Numeric entry (e.g. 25, 30). *Validation:* Must be ≥25 (eligibility) and ≤80 (plausible upper bound). *Missing/Data Code:* ‘999’ = Prefer not to answer.  
- **A2. Birth Year (B_YEAR):** *Type:* Continuous (year). *Definition:* Year of birth (optional cross-check). *Question:* “What year were you born?” *Response:* Four-digit year (e.g. 1985). *Usage:* Derived Age = 2026 - B_YEAR. *Missing Code:* 9999 = No response.  
- **A3. Province (PROV):** *Type:* Categorical. *Definition:* Province or federal territory of residence. *Options:* Punjab (1), Sindh (2), Khyber Pakhtunkhwa (3), Balochistan (4), Islamabad (5), Gilgit-Baltistan (6), Azad Jammu & Kashmir (7). *Question:* “In which province or region do you currently live?” *Response:* Single choice. *Derived:* Region dummy variables (e.g. PROV_PUNJAB = 1 if Punjab, else 0). *Missing:* 98 = Not stated.  
- **A4. City/Town (CITY):** *Type:* Text or Categorical. *Definition:* Name of city or town (or rural area) of residence. *Question:* “What is the name of your city or town of residence?” *Response:* Open text or selection if lists used. *Usage:* Can categorize urban centers vs. others (e.g., major cities list). *Validation:* If “urban” city given → URBAN=1, if rural/village → URBAN=0.  
- **A5. Urban/Rural (URBAN):** *Type:* Binary (0/1). *Definition:* Urban (1) vs. rural (0) area of residence. *Derived:* Based on CITY or self-report. *Question:* If needed: “Do you live in an urban city/town (1) or a rural area/village (0)?” *Missing:* 9 = Don’t know.  
- **A6. Ethnicity (ETHNIC):** *Type:* Categorical. *Definition:* Self-identified ethnic group. *Options:* Punjabi, Sindhi, Pashtun, Baloch, Kashmiri, Others (including Muhajir, Hazara, etc.). *Question:* “Which ethnic or cultural group do you consider yourself a member of?” *Response:* Single choice from list. *Missing:* 98 = Not stated.  
- **A7. Religion (RELIGION):** *Type:* Categorical. *Definition:* Religious affiliation. *Options:* Islam (Sunni [1], Shia [2]), Christianity [3], Hinduism [4], Others [5]. *Question:* “What is your religious affiliation?” *Response:* Single choice. *Missing:* 99 = Prefer not to say.  
- **A8. Primary Language (LANG):** *Type:* Categorical. *Definition:* Mother tongue or primary language spoken. *Options:* Urdu [1], Punjabi [2], Sindhi [3], Pashto [4], Balochi [5], English [6], Other (specify) [7]. *Question:* “What is your first language or mother tongue?” *Response:* Single choice.  
- **A9. Education Level (EDU_LEVEL):** *Type:* Ordinal. *Definition:* Highest formal education attained. *Options:* Bachelor’s degree [4], Master’s [5], MPhil/Other Postgrad [6], PhD [7], Other (Diploma, professional degree) [3]. (Assign numbers proportionally or use labels.) *Question:* “What is your highest level of education completed?” *Response:* Single choice from formal degrees. *Coding:* 4=BA/BSc, 5=MA/MSc, 6=Professional (MBA, etc.), 7=MPhil, 8=PhD.  
- **A10. Professional Qualification (QUAL):** *Type:* Categorical (multiple possible). *Definition:* Professional certifications or degrees (e.g. engineering license, chartership). *Question:* “Do you hold any professional qualifications/certificates? If yes, please specify (e.g., Engineer license, CA, ACCA, etc.).” *Response:* Open text or multiple check. *Usage:* Derive indicators such as HAS_PROF_CERT (Y/N).  
- **A11. Marital Status (MARITAL):** *Type:* Categorical. *Definition:* Current marital/legal relationship status. *Options:* Married [1], Never Married [2], Divorced [3], Widowed [4], Separated/Annulled [5]. *Question:* “What is your current marital status?” *Response:* Single choice. *This variable is crucial for cohort assignment.*  
- **A12. Years Married (YRS_MARR):** *Type:* Continuous. *Definition:* Number of years since first marriage. *Question:* “If married, how many years have you been married?” *Response:* Numeric. *Applicable only if MARITAL=Married.* *Missing:* 99=Not applicable.  
- **A13. Age at First Marriage (AGE_MARR):** *Type:* Ordinal. *Definition:* Age when first married (even if no longer married). *Question:* “If ever married, how old were you when you first got married?” *Response:* Numeric (or age bracket). *Valid if MARITAL ≠ Never.* *Missing:* 99=N/A.  
- **A14. Number of Children (NUM_CHILD):** *Type:* Ordinal/Count. *Definition:* Number of living children. *Question:* “How many living children do you have?” *Response:* Numeric count (0,1,2,...). *Derived Binary:* CHILDREN_YN = 1 if NUM_CHILD ≥1, else 0.  
- **A15. Dependents (NUM_DEP):** *Type:* Ordinal. *Definition:* Number of other dependents (elderly, disabled). *Question:* “Aside from your children, do you have any dependents (e.g. elderly parents, disabled relatives)? If yes, how many?” *Response:* Numeric (0,1,2,...). *Used to compute Caregiving Index.*  
- **A16. Household Income Bracket (INC_BRAC):** *Type:* Categorical. *Definition:* Combined monthly household income. *Options:* e.g., <30,000 [1], 30k–60k [2], 60k–100k [3], 100k–200k [4], >200k [5] (in PKR). *Question:* “Which range best describes your total monthly household income?” *Response:* Single choice. *Missing:* 98 = Prefer not to say.  
- **A17. Personal Income (PERS_INC):** *Type:* Categorical. *Definition:* Respondent’s own monthly income bracket. *Options:* similar to above or specific ranges. *Question:* “Which range best describes your own monthly income from all sources?” *Response:* Single choice.  
- **A18. Home Ownership (HOMEOWN):** *Type:* Binary. *Definition:* Whether respondent or family owns their home. *Question:* “Do you (or your immediate family) own your residence? (Yes=1, No=0)” *Response:* Binary choice.  
- **A19. Material Assets (ASSETS_SCORE):** *Type:* Index (derived). *Definition:* Count of durable assets owned (e.g., car, computer, savings >X, etc.). *Computation:* Sum of items like car=1, computer=1, etc. *Question:* “Do you or your household own the following: car, motorbike, computer/laptop, fridge, internet connection, etc.? (Yes/No each)” *Usage:* Higher score indicates greater economic capital.  
- **A20. Caste/Clan (CASTE):** *Type:* Categorical. *Definition:* Self-identified caste or clan, if relevant in context. *Question:* “To which caste or clan do you belong? (If unknown or not applicable, write ‘Other’ or ‘None’.)” *Response:* Open text or categories (Sindhi, etc.). *Note:* Optional, sensitive; may skip or use only if culturally appropriate.  
- **A21. Urbanity Index (URBINDEX):** *Type:* Derived (binary/integer). *Definition:* Derived composite measure of urbanization (e.g., city size + amenities). *Computation:* Example: assign points for living in major metro, access to public transport, etc. *Use:* As continuous measure of urban advantage.  
- **A22. Education Field (EDU_FIELD):** *Type:* Categorical. *Definition:* Field/major of highest degree (e.g. Science, Social Science, Business, Engineering, Arts, Medicine, Law, Education, etc.). *Question:* “What was your major field of study for your highest degree?” *Response:* Single choice.  

*Coding Conventions:* All categorical variables should have a codebook entry. Numeric values should use ‘9’s for missing: e.g., 98 or 99 for “Don’t know/Prefer not to answer.” If multiple categories exceed 8, use numeric codes accordingly.

*Missing-Data Rules:* If a respondent declines to answer or question skipped, code as specified (e.g., 98/99). Use soft reminders to re-ask and verify. For inconsistent ages (e.g., AGE < education years), check logic.

---

## Domain B: Family Ecology

**Purpose:** To measure family structure, dynamics, and expectations, including support and pressure from relatives.

- **B1. Family Structure (FAM_STRUC):** *Type:* Categorical. *Definition:* Current household living arrangement. *Options:* Nuclear family [1], Joint/Extended family [2], Living alone [3], Other [9]. *Question:* “Which best describes your current household arrangement?” *Response:* Single choice.  
- **B2. Household Members (HH_MEM):** *Type:* Integer. *Definition:* Total number of people in household (including respondent). *Question:* “Including yourself, how many people live in your household?” *Response:* Numeric. *Use:* To understand family size.  
- **B3. Parents Co-resident (PARENTS_RES):** *Type:* Binary. *Definition:* Whether respondent lives with one or both parents. *Question:* “Do you live with any of your parents? (Yes=1, No=0)” *Response:* Binary. *If Yes,* “Which parent(s)?” [Mother only, Father only, Both].  
- **B4. Parent Expectations (PARENT_EXP):** *Type:* Ordinal scale. *Definition:* Degree of marriage pressure from parents. *Question:* “My parents frequently pressure me to get married.” *Response:* 5-point Likert (1=Strongly Disagree … 5=Strongly Agree). *Coding:* Sum into Parent Pressure Score (higher = more pressure).  
- **B5. In-Laws Influence (INLAWS_INF):** *Type:* Ordinal. *Definition:* Influence of in-laws (if married) on decisions. *Question:* “My in-laws actively involve themselves in decisions about my life (career, household, etc.).” *Response:* 5-point Likert. *Applicable:* Only if MARITAL=Married; else code as 99.  
- **B6. Extended Family Expectations (EXTFAM_EXP):** *Type:* Ordinal. *Definition:* General family/community expectations about the respondent’s social roles. *Question:* “My extended family and relatives have clear expectations for my life choices (e.g., marriage, children, career).” *Response:* 5-point Likert.  
- **B7. Family Support (FAM_SUPPORT):** *Type:* Ordinal scale. *Definition:* Degree of emotional/financial support received from family. *Question:* “My family is supportive of my career and personal goals.” *Response:* 5-point Likert. *Derived:* Family Support Index (sum of several supportive-statement items).  
- **B8. Parental Education (P_EDU):** *Type:* Ordinal. *Definition:* Highest education level of mother. *Options:* None [0], Primary [1], Secondary [2], College [3], Graduate [4], Unknown [9]. *Question:* “What is the highest education level your mother completed?” *Response:* Single choice. *Derived:* SES indicator.  
- **B9. Parental Occupation (P_OCC):** *Type:* Categorical. *Definition:* Main occupation of household head/parent (profession, agriculture, trade, unemployed, etc.). *Question:* “What is/was your father’s (or family head’s) main occupation?” *Response:* Open text or coded.  
- **B10. Sibling Count (SIB_COUNT):** *Type:* Integer. *Definition:* Number of siblings (brothers + sisters). *Question:* “How many siblings (brothers and sisters) do you have?” *Response:* Numeric. *Use:* Family dependency pattern.  
- **B11. Sibling Support (SIB_SUPPORT):** *Type:* Binary. *Definition:* Whether any sibling provides support. *Question:* “Do any of your siblings contribute support (financial or caregiving) to you or your household?” *Response:* Yes=1/No=0.  
- **B12. Family Honor Pressure (HONOR_PRES):** *Type:* Ordinal. *Definition:* Pressure to uphold family reputation/traditions. *Question:* “I feel pressure to uphold my family’s honor in my personal and professional life.” *Response:* 5-point Likert.  
- **B13. Family Size at Birth (BIRTH_ORDER):** *Type:* Ordinal. *Definition:* Birth order (e.g., 1st, 2nd, etc.). *Question:* “What was your birth order among your siblings?” *Response:* Numeric (1=oldest, 2=second, etc.). *Derived:* BirthOrderIndicator (1=firstborn, 0=others).  
- **B14. Marital Family Income (MARR_INCM):** *Type:* Categorical. *Definition:* Combined income if married/spouse. *Question:* “If married, what is the combined monthly income of you and your spouse?” *Response:* Income brackets (same as household). *Applicability:* MARITAL=Married. *Missing:* 99 if not married.  
- **B15. Kinship Support Index (KIN_SUPPORT):** *Type:* Index (derived). *Definition:* Composite measure of support from extended relatives (e.g. how often relatives help in emergencies, gifts, advice). *Question:* Series of items (e.g., “My relatives are willing to help me in an emergency,” 5-pt Likert). *Computation:* Sum or average of items (range 3–15). *Missing:* Compute only if ≥2 items answered.  

*Missing-Data and Validation:* For all family ecology items, allow “Not Applicable” (code 98) if circumstance is irrelevant (e.g., no spouse, no siblings), and “Don’t Know” (code 99) for factual items (parents’ occupation) if unknown.

---

## Domain C: Relationship Ecology

**Purpose:** To capture the respondent’s current and past intimate relationship status and related dynamics.

- **C1. Current Relationship Status (REL_STATUS):** *Type:* Categorical. *Definition:* Clarifies marital status from Domain A with detail. *Options:* Married [1], In a serious relationship (cohabiting/engaged) [2], Single [3] (no partner), Other [9]. *Question:* “What best describes your current romantic situation?” *Response:* Single choice.  
- **C2. Number of Long-term Relationships (REL_HISTORY):** *Type:* Integer. *Definition:* Count of serious dating or engagement relationships (excluding marriage) lasting >6 months. *Question:* “How many long-term relationships have you had (lasting at least 6 months)?” *Response:* Numeric.  
- **C3. Partner’s Education (PART_EDU):** *Type:* Ordinal. *Definition:* Highest education of current spouse/partner. *Question:* “What is the highest education level attained by your spouse/partner?” *Response:* Similar scale as EDU_LEVEL. *Applicable:* if REL_STATUS is Married or serious relationship. *Missing:* 99 if not applicable.  
- **C4. Partner’s Occupation (PART_OCC):** *Type:* Categorical. *Definition:* Occupation of spouse/partner (profession, business, etc.). *Question:* “What is your spouse’s or partner’s occupation?” *Response:* Coded (professional categories). *Missing:* 99 if no partner.  
- **C5. Marriage/Relationship Satisfaction (MARR_SAT):** *Type:* Ordinal. *Definition:* Overall satisfaction with marriage/relationship. *Question:* “Overall, how satisfied are you with your marriage/relationship?” *Response:* 5-point Likert (1=Very Dissatisfied to 5=Very Satisfied). *Applicability:* Married or in relationship; code 98 if single.  
- **C6. Spousal Support (SPOUSE_SUP):** *Type:* Ordinal. *Definition:* Perceived support (emotional, financial) from spouse/partner. *Question:* “My spouse/partner supports me in my personal and professional goals.” *Response:* 5-point Likert. *Applicability:* Married or similar; else 98.  
- **C7. Conflict with In-Laws (INLAW_CONFLICT):** *Type:* Ordinal. *Definition:* Frequency of serious conflicts with in-laws. *Question:* “How often do you have serious arguments or conflicts with your in-laws?” *Response:* 5-point scale (1=Never to 5=Very Often). *Applicability:* If married; else 98.  
- **C8. Number of Proposals (PROP_COUNT):** *Type:* Integer. *Definition:* Number of marriage proposals received (ever). *Question:* “How many marriage proposals have been formally offered to you by suitors?” *Response:* Numeric. *Use:* Proxy for social demand for marriage.  
- **C9. Voluntary Singleness (SINGLE_CHOICE):** *Type:* Binary. *Definition:* Whether the respondent has chosen to remain unmarried. *Question:* “Did you decide by personal choice to remain unmarried at this time (Yes=1, No=0)?” *Response:* Yes/No. *Note:* For analysis of autonomy.  
- **C10. Relationship History Quality (REL_QUAL):** *Type:* Ordinal. *Definition:* Perception of past relationships ending (if applicable). *Question:* “If you have had previous marriages or relationships, how would you rate the overall quality of those relationships?” *Response:* 5-point (Very Poor to Very Good). *Applicability:* If REL_HISTORY>0 or MARITAL not first marriage. *Missing:* 98 if none.  
- **C11. Family Approval of Partner (APPROVAL):** *Type:* Ordinal. *Definition:* Degree of family (parents/in-laws) approval of spouse/partner. *Question:* “My family approves of my spouse/partner.” *Response:* 5-point Likert. *Applicability:* If married or relationship. *Missing:* 98 if no partner.  
- **C12. Bridal Pressure (BRIDE_PRESS):** *Type:* Ordinal. *Definition:* Pressure experienced from bride’s side (if engaged). *Question:* “Have you felt pressure from your partner’s family to meet their expectations (e.g., regarding wedding, role)?” *Response:* 5-point Likert. *Applicability:* Engaged/married. *Missing:* 98 if irrelevant.  

*Notes:* These variables capture both objective relationship status and subjective quality. Questions use 5-point Likert scales. Reverse-code negative statements consistently (higher values = more positive/support). Use ’98=Not Applicable’ and ‘99=Unknown/No answer’ as needed.

---

## Domain D: Parenthood Ecology

**Purpose:** To quantify parenting responsibilities, experiences, and related pressures for mothers.

- **D1. Number of Children (NUM_CHILD):** *Type:* Integer. *Definition:* Total living children (duplicate of A14). *Validation:* Cross-checked with “Number of sons/daughters.” *Question:* “How many living children do you have?” *Response:* Numeric.  
- **D2. Children’s Ages (CHILD_AGE):** *Type:* Continuous list. *Definition:* Ages of each child. *Question:* “Please specify the age of each of your children.” *Response:* Numeric for each (e.g., 5, 8, 12). *Usage:* Compute average or age of youngest.  
- **D3. Youngest Child Age (YNGEST_AGE):** *Type:* Continuous. *Definition:* Age of the youngest child (if any). *Derived from CHILD_AGE entries. *Missing:* 99 if no children.  
- **D4. Parenting Hours (PAR_HOURS):** *Type:* Continuous. *Definition:* Average hours per week spent on childcare (bathing, feeding, supervising, etc.). *Question:* “On a typical week, how many hours do you spend caring for your children?” *Response:* Numeric hours. *Validation:* If >100, re-check. *Missing:* 999 if no children.  
- **D5. School/Childcare Arrangements (SCHOOL_TYPE):** *Type:* Categorical. *Definition:* Type of schooling or childcare for each child (public, private, home-school, day-care, etc.). *Question:* “For each child, select the type of school or daycare they attend.” *Response:* Multiple entries (one per child). *Usage:* Categorical breakdown of childcare type.  
- **D6. Parenting Stress (PARENT_STRESS):** *Type:* Ordinal. *Definition:* Level of stress associated with parenting duties. *Question:* “I often feel stressed by the demands of parenting.” *Response:* 5-point Likert. *Applicable:* If NUM_CHILD ≥1; else 98. *Derived:* Part of Psychological Wellbeing domain.  
- **D7. Work–Family Conflict (WF_CONFLICT):** *Type:* Ordinal. *Definition:* Extent to which work interferes with family life. *Question:* “My work responsibilities make it difficult to fulfill my roles at home (e.g. missing family events).” *Response:* 5-point Likert. *If no children, applicable for any family duty.  
- **D8. Parenting Satisfaction (PARENT_SAT):** *Type:* Ordinal. *Definition:* Overall satisfaction with parenting. *Question:* “Overall, how satisfied are you with your role as a parent?” *Response:* 5-point Likert (1=Very dissatisfied to 5=Very satisfied). *Applicability:* If NUM_CHILD>0.  
- **D9. Co-parent Support (COPARENT_SUP):** *Type:* Ordinal. *Definition:* Spouse/partner’s support in parenting (if co-parent exists). *Question:* “My spouse/partner actively helps with childcare and parenting duties.” *Response:* 5-point Likert. *Applicability:* Married women with children; else 98.  
- **D10. Child Healthcare (HEALTHCARE):** *Type:* Binary. *Definition:* Access to regular healthcare for children (Yes/No). *Question:* “Do your children have regular check-ups at a medical clinic or hospital?” *Response:* Yes=1/No=0. *Applicability:* If NUM_CHILD>0. *Follow-up:* If No, ask “Why not?” (e.g. cost, time, distance).  
- **D11. Child Education Investment (EDU_INV):** *Type:* Ordinal. *Definition:* Parents’ investment in children’s education (relative to peers). *Question:* “I am able to invest in my children’s education (tutors, supplies, school fees) at a level comparable to other families in my community.” *Response:* 5-point Likert.  
- **D12. Single Mother Status (SINGLE_MOM):** *Type:* Binary. *Definition:* Whether the respondent is raising children without spouse/partner. *Question:* “Are you raising your child(ren) as a single parent (without a spouse/partner)? (Yes=1, No=0)” *Response:* Yes/No. *Applicability:* If NUM_CHILD>0 and MARITAL ≠ Married.  
- **D13. Care Dependency Index (CARE_DEP):** *Type:* Derived index. *Definition:* A composite score reflecting caregiving burden, combining hours of care (D4), single-parent status (D12), and number/age of young children. *Formula Example:* CARE_DEP = (PAR_HOURS/168) + (NUM_CHILD * 0.2) + (SINGLE_MOM * 0.5). *Range:* Normalized 0–some scale (for analysis).

---

## Domain E: Caregiving Ecology

**Purpose:** To quantify responsibilities for non-parent caregiving, a significant factor in women’s stress and time use.

- **E1. Elderly Dependents (ELDER_YN):** *Type:* Binary. *Definition:* Whether respondent provides daily care for any elderly family member (age ≥60). *Question:* “Do you regularly provide care for an elderly relative (parent or in-law) on a daily/weekly basis? (Yes=1, No=0)” *Response:* Yes/No.  
- **E2. Number of Elders (NUM_ELDER):** *Type:* Integer. *Definition:* Number of elderly dependents cared for. *Question:* “How many elderly persons in your household or family do you care for?” *Response:* Numeric (0 if none). *Applicability:* If ELDER_YN=1.  
- **E3. Elder Care Hours (ELDER_HRS):** *Type:* Continuous. *Definition:* Hours per week spent on elder care (medication, feeding, supervision). *Question:* “Approximately how many hours per week do you spend caring for the elderly relative(s)?” *Response:* Numeric hours. *Validation:* If >100, double-check. *Missing:* 999 if none.  
- **E4. Disabled Dependents (DISABLE_YN):** *Type:* Binary. *Definition:* Whether respondent cares for any disabled or chronically ill dependent. *Question:* “Do you care for any household member who is disabled or chronically ill?” *Response:* Yes/No.  
- **E5. Caregiving Stress (CARE_STRESS):** *Type:* Ordinal. *Definition:* Subjective stress due to caregiving duties (elder or disabled). *Question:* “I often feel overwhelmed by my caregiving responsibilities (for elders or disabled family).” *Response:* 5-point Likert. *Applicable:* If ELDER_YN=1 or DISABLE_YN=1; else 98.  
- **E6. Formal Care Assistance (FORMAL_CARE):** *Type:* Binary. *Definition:* Usage of professional caregiving services (e.g. hired help, nursing homes). *Question:* “Do you employ any professional caregiver or use any care facility for your dependents?” *Response:* Yes=1/No=0. *Missing:* 9 if not applicable.  
- **E7. Caregiving Support Network (CARE_NET):** *Type:* Ordinal. *Definition:* Extent of help received from others for caregiving. *Question:* “I have support from other family members or friends to help with caregiving duties.” *Response:* 5-point Likert. *Derived:* Part of social support analysis.  
- **E8. Caregiving Opportunity Cost (OPPORT_COST):** *Type:* Ordinal. *Definition:* Impact of caregiving on work/career. *Question:* “My caregiving responsibilities have prevented me from pursuing some job opportunities.” *Response:* 5-point Likert. *Use:* To quantify career sacrifice.  
- **E9. Caregiving Index (CARE_IDX):** *Type:* Derived. *Definition:* Combined measure of total caregiving burden. *Formula Example:* CARE_IDX = (Elder_Care_Hours/168 + Disabled_Care_Hours/168) * 50 + (NUM_ELDER + NUM_DISABLE). *Normalization:* Scale 0–100. *Purpose:* A continuous covariate representing overall caregiving load.  

*Missing-Data Rules:* If no elder/disabled to care for, code caregiving stress and related items as ‘Not Applicable’ (98). Encourage respondents to quantify caregiving hours; allow ranges if exact count is difficult.

---
