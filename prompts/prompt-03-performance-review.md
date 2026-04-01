# Prompt 03 — Performance Review Summary

**Business Field:** Retail HR Operations  
**Workflow Task:** Annual Performance Documentation  
**Current Version:** v1.2 

---

## Version History

### v1.0 — Initial Draft

#### Prompt Text

Summarise an employee performance review.


#### Intended Workflow or Task
Post-review documentation step — manager completes review, HR drafts formal summary for the employee file.

#### Problem Being Solved
Managers spend approximately 90 minutes per annual review writing summaries. With 800 staff on annual review cycles, this is 1,200 hours per year of management time.

#### Automation Potential
Very low — no context provided; output is meaningless without real performance data.

#### Risks and Limitations
AI may invent performance data with no safeguard in place. Completely unusable as a business document. Risk of fabricated achievements or development areas being included.

---

### v1.1 — Added Structured Input and RACE Role

**What changed:** Added RACE role framing, structured manager notes as input, and 3 required output sections including a rating recommendation.  
**Observed effect:** Usable draft produced from real data. However, HR manager flagged the automated rating recommendation as too prescriptive and potentially dangerous.  
**Lesson learned:** Remove AI from rating decisions entirely — keep it as a drafting tool only.

#### Prompt Text
```
You are an HR business partner. Based on the following performance notes for [EMPLOYEE_NAME] ([JOB_TITLE]), write a professional performance review summary: [MANAGER_NOTES]. Include: key achievements, areas for development, and recommended rating.
```

#### Intended Workflow or Task
Manager submits review notes via HR portal. Prompt takes notes as input and generates draft summary. HR partner reviews before sharing with employee.

#### Problem Being Solved
Managers spend approximately 90 minutes per annual review on documentation. At 800 staff, this is 1,200 hours per year — 30 FTE weeks of managerial time diverted from team leadership.

#### Automation Potential
Medium — structured output from real input. However, the automated rating recommendation is risky and may conflict with manager judgement.

#### Risks and Limitations
AI rating recommendation may conflict with manager judgement and be adopted without proper review. Employee data is sensitive and requires careful handling. Risk of cultural or gender bias in language if not reviewed carefully.

---

### v1.2 — Final Version 

**What changed:** Removed rating recommendation, added review period field, added explicit privacy exclusions, set 280-word cap.  
**Observed effect:** HR Manager approved format for use. Output used directly in 12 pilot reviews with minor edits only.  
**Lesson learned:** AI should draft, not decide — especially on sensitive HR matters like performance ratings.

#### Prompt Text
```
You are an HR business partner. Using the manager's performance notes below, draft a professional, balanced performance review summary for [EMPLOYEE_NAME] ([JOB_TITLE]) covering the review period [PERIOD]. Structure the output: (1) Summary of Performance (3 sentences), (2) Key Achievements (3 bullet points with evidence), (3) Development Areas (2 areas with recommended actions), (4) Suggested Focus for Next Period (2 sentences). Do not recommend a performance rating — this is the manager's decision. Maximum 280 words. Tone: professional, constructive, specific. Do not include salary, disciplinary history, or personal details.

Manager Notes: [MANAGER_NOTES]
```

#### Intended Workflow or Task
Triggered after manager completes review form in HR portal. HR business partner provides manager notes as input, reviews AI draft, and shares with employee only after manager approval.

#### Problem Being Solved
Managers spend approximately 90 minutes per annual review on documentation. At 800 staff, this is 1,200 hours per year — equivalent to 30 FTE weeks of management time per review cycle with no strategic value.

#### Automation Potential
**High** — estimated 70% time reduction per review (90 min → ~25 min). Rating decision retained entirely with manager. Human review mandatory before sharing with employee.

#### Risks and Limitations
- **Fabrication Risk:** If manager notes are thin, AI may over-interpret or invent achievements. *Mitigation: HR partner cross-checks all claims against source notes before use.*
- **Privacy:** Employee performance data is sensitive. Notes must not include disciplinary history, health information, or personal circumstances. Pre-prompt data scrub required.
- **Bias:** AI may introduce cultural or gender bias in phrasing. *Mitigation: HR partner reviews tone and language before distribution to employee.*

---

## Audit Log

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No input data, no structure | Meaningless generic output; unusable | Performance prompts need real data as input |
| v1.1 | Added RACE, structured input, rating section | Usable draft but rating section flagged as risky by HR Manager | Remove AI from rating decisions entirely |
| v1.2 | Removed rating, privacy exclusions, word cap | HR-approved; used successfully in 12 pilot reviews | AI drafts, humans decide on sensitive matters |
