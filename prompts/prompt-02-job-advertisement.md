# Prompt 02 — Job Advertisement: Retail Vacancy

**Business Field:** Retail HR Operations  
**Workflow Task:** Recruitment Advertising  
**Current Version:** v1.2 

---

## Version History

### v1.0 — Initial Draft

#### Prompt Text
```
Write a job ad for a retail store manager.
```

#### Intended Workflow or Task
First step in the recruitment pipeline when a vacancy is confirmed by store management.

#### Problem Being Solved
Recruitment coordinators spend approximately 60 minutes per vacancy drafting job ads. At 440 vacancies per year, this represents 440 hours of coordinator time annually.

#### Automation Potential
Very low — output too vague, missing legal requirements and brand tone. Full rewrite required.

#### Risks and Limitations
No constraint on discriminatory language. Ad may attract unsuitable candidates and expose the company to EEO compliance risk.

---

### v1.1 — Added RACE Role and Three Required Sections

**What changed:** Added RACE role framing, Australian business context, and 3 required output sections.  
**Observed effect:** Significantly better structure. However, no EEO clause, no salary field, and benefits were occasionally omitted.  
**Lesson learned:** Legal compliance elements (EEO) and salary must be explicit requirements in the prompt.

#### Prompt Text
```
You are an HR recruitment specialist for an Australian retail chain. Write a job advertisement for a [JOB_TITLE] position at [STORE_LOCATION]. Include responsibilities, qualifications required, and what the company offers. Use an engaging, professional tone.
```

#### Intended Workflow or Task
Triggered when vacancy is confirmed in the ATS. Recruitment coordinator inputs role details and reviews output before posting to Seek or LinkedIn.

#### Problem Being Solved
Approximately 60 minutes per vacancy for drafting. At 440 vacancies per year, this is 440 hours — nearly 11 FTE weeks per year of low-value writing work.

#### Automation Potential
Medium — improved structure but no EEO language, no salary placeholder, and inconsistent length across outputs.

#### Risks and Limitations
No explicit EEO or inclusion language. Risk of unintentionally exclusive language if not prompted. Output length inconsistent between runs, making review time unpredictable.

---

### v1.2 — Final Version 

**What changed:** Added EEO requirement, salary placeholder, 350-word cap, exclusion of internal data.  
**Observed effect:** Legal compliance elements now consistently present. Outputs post-ready with 15 min review.  
**Lesson learned:** Compliance elements must be mandated in prompt, not assumed by AI.

#### Prompt Text
```
You are a recruitment specialist for an Australian retail chain. Write a job advertisement for a [JOB_TITLE] at [STORE_LOCATION]. Structure the ad with these exact sections: (1) Role Overview (3 sentences), (2) Key Responsibilities (5 bullet points), (3) What We Are Looking For (4 criteria), (4) What We Offer (3 benefits), (5) How to Apply (2 sentences). Include EEO statement: "We welcome applications from people of all backgrounds." Salary range: [SALARY_RANGE]. Maximum 350 words. Use an engaging but professional tone. Do not include specific names of managers or internal HR codes.
```

#### Intended Workflow or Task
Triggered in ATS when vacancy is approved. Coordinator inputs `[JOB_TITLE]`, `[STORE_LOCATION]`, and `[SALARY_RANGE]`. Output reviewed and posted to Seek and LinkedIn within 2 hours.

#### Problem Being Solved
Recruitment coordinators spend approximately 60 minutes per vacancy drafting job ads. At 440 vacancies per year, this represents 440 hours — 11 FTE weeks — of repetitive low-value drafting annually.

#### Automation Potential
**High** — estimated 75–85% time reduction per vacancy. EEO compliance built into template. Scalable across all roles and locations. Coordinator review (~15 min) retained before publishing.

#### Risks and Limitations
- **Bias Risk:** Without explicit EEO exclusions, AI may generate exclusionary language. *Mitigation: EEO clause mandated in prompt; coordinator screens output before posting.*
- **Accuracy Risk:** AI may fabricate benefits or responsibilities if role context is thin. *Mitigation: Coordinator validates all content against role brief before posting.*

---

## Audit Log

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | Minimal — role name only | Vague generic output; no legal elements | Role specs and tone constraints essential |
| v1.1 | Added RACE role and 3 sections | Better structure; no EEO clause | Legal requirements must be explicit |
| v1.2 | Added EEO, salary field, word cap, section structure | Compliance-ready output; 15 min review sufficient | Mandate all legal and format requirements in prompt |
