# Prompt 01 — Welcome Email: New Hire Onboarding

**Business Field:** Retail HR Operations  
**Workflow Task:** HR Onboarding Communication  
**Current Version:** v1.2 

---

## Version History

### v1.0 — Initial Draft

#### Prompt Text
```
Write a welcome email for a new employee.
```

#### Intended Workflow or Task
Step 1 of the onboarding sequence — sent to new hire once contract is signed.

#### Problem Being Solved
HR coordinators spend approximately 45 minutes per hire drafting welcome emails manually. At 55% annual turnover across 800 staff, this recurs roughly 440 times per year — approximately 330 hours of coordinator time annually.

#### Automation Potential
Low — output too generic to use without a full rewrite. Human rewrite time approximately 40 minutes per email.

#### Risks and Limitations
Minimal personalisation means low trust from the new hire. No governance issue but no meaningful time saving is achieved. Risk of tone misalignment with company brand.

---

### v1.1 — Added RACE Framework and Section Structure

**What changed:** Added RACE role framing, specified business context, and listed 4 required sections.  
**Observed effect:** Tone improved significantly; output structure more consistent. However emails were sometimes 400+ words — too long for a welcome message.  
**Lesson learned:** Output format constraints (word limit, excluded content) are essential for business-ready outputs.

#### Prompt Text
```
You are an HR onboarding specialist at a mid-size Australian retail company. Write a warm, professional welcome email for a new [JOB_TITLE] joining [STORE_NAME] on [START_DATE]. Include: a warm welcome, role overview, first-week schedule, and key contacts.
```

#### Intended Workflow or Task
Step 1 of onboarding chain — triggered when HRIS confirms new hire. HR coordinator reviews and sends within 24 hours of confirmation.

#### Problem Being Solved
HR coordinators spend approximately 45 minutes per hire drafting welcome emails. At 55% annual turnover, that is approximately 330 hours per year — equivalent to 8+ weeks of one FTE's time.

#### Automation Potential
Medium — output improved significantly but inconsistent length and no word limit. Human edit time approximately 15 minutes.

#### Risks and Limitations
RACE framework improves tone but lack of a length constraint produces variable outputs. Risk of over-length emails reducing readability. No PII included beyond name, role, and date.

---

### v1.2 — Final Version 

**What changed:** Added 220-word limit, numbered section structure, explicit content exclusion (salary/contract).  
**Observed effect:** Consistent, business-ready outputs in 9 min review time. Format constraints eliminated length variability.  
**Lesson learned:** Format constraints + explicit exclusions = reliable, deployable outputs.

#### Prompt Text
```
You are an HR onboarding specialist at a mid-size Australian retail chain. Draft a warm, professional welcome email for a new [JOB_TITLE] joining [STORE_NAME] on [START_DATE]. Include: (1) warm welcome paragraph, (2) brief role overview (2 sentences), (3) first-week schedule highlights, (4) key contacts with names and roles, (5) one motivational closing sentence. Maximum 220 words. Do not include salary, contract, or payroll details.
```

#### Intended Workflow or Task
Step 1 of HR onboarding chain. Triggered automatically when new hire status confirmed in HRIS. HR coordinator reviews output, personalises if needed, and sends within 24 hours.

#### Problem Being Solved
HR coordinators spend approximately 45 minutes per hire on this task. At 55% annual turnover across 800 staff, that equates to approximately 330 hours per year — equivalent to 8+ FTE weeks of repetitive drafting with no strategic value.

#### Automation Potential
**High** — estimated 80% time reduction per hire (45 min → ~9 min review). Scalable across all 40 store locations. Human review retained before sending to catch errors or tone issues.

#### Risks and Limitations
- **Hallucination Risk:** If HRIS placeholder variables (`[JOB_TITLE]`, `[STORE_NAME]`, `[START_DATE]`) are empty or malformed, the AI may fabricate plausible-sounding but incorrect details. *Mitigation: validate all placeholders before prompt executes; add mandatory pre-send human check.*
- **Privacy:** No PII beyond name, role, and date. Do not pass salary, contract terms, or personal details into the prompt.

---

## Audit Log

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | Initial — broad instruction only | Output generic; unusable without full rewrite | Need role framing and output structure |
| v1.1 | Added RACE role + 4 section headings | Better tone; variable length | Add explicit format constraints |
| v1.2 | Word limit + exclusions + numbered structure | Consistent, business-ready output in 9 min review | Format constraints = reliable outputs |
