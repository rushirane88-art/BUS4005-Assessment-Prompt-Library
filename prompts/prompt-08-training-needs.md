# Prompt 08 — Training Needs Analysis Summary

**Business Field:** Retail HR Operations  
**Workflow Task:** Learning and Development Planning  
**Current Version:** v1.2 

---

## Version History

### v1.0 — Initial Draft

#### Prompt Text

Identify training needs for retail staff.


#### Intended Workflow or Task
Annual L&D planning — identifying skill gaps to inform the training budget and calendar for the coming year across all 40 stores.

#### Problem Being Solved
L&D coordinator spends approximately 2 hours per team synthesising training needs from manager feedback forms. This occurs quarterly across 40 stores — approximately 320 hours per year.

#### Automation Potential
Very low — no data input provided; AI generates generic training topics entirely disconnected from actual team needs.

#### Risks and Limitations
Generic training recommendations waste budget on low-priority topics. No connection to real performance data. Output could lead to misdirected investment in irrelevant programs.

---

### v1.1 — Added Structured Input and RACE Role

**What changed:** Added RACE role framing, structured manager feedback as input, and a recommendation with justification requirement.  
**Observed effect:** Useful and relevant output produced from real data. However, L&D manager noted the absence of business impact framing — without it, the output was not suitable for executive budget approval submissions.  
**Lesson learned:** Add business impact framing to make recommendations actionable for senior leadership and budget decision-makers.

#### Prompt Text

You are an L&D specialist. Based on the following manager feedback, identify the top training needs for the [TEAM] team at [STORE_NAME]. Feedback: [MANAGER_FEEDBACK]. Recommend training priorities and justify each.


#### Intended Workflow or Task
L&D coordinator inputs manager feedback after quarterly reviews. AI identifies patterns and recommends priorities for inclusion in HR planning and budget requests.

#### Problem Being Solved
2 hours per store per quarter across 40 stores equals 320 hours per year of manual synthesis. Training plans are often misaligned with actual skill gaps as a result of limited analysis capacity.

#### Automation Potential
Medium — useful output from real data but no business impact language to support budget approval. Recommendations useful internally but not ready for executive audience without significant rewriting.

#### Risks and Limitations
Recommendations may reflect what managers report rather than actual evidence-based performance gaps. AI cannot distinguish between perception and measurable performance data. Output not yet suitable for budget submission without further development.

---

### v1.2 — Final Version 

**What changed:** Added business impact per priority, recommended training format, effort estimate in hours, anonymisation instruction, and 350-word cap.  
**Observed effect:** GM People and Culture used the first quarterly output directly for budget approval. Approved in a single meeting versus the previous multi-week process.  
**Lesson learned:** Business impact framing transforms AI summaries into decision-ready documents that senior leadership can act on directly.

#### Prompt Text

You are an L&D specialist preparing a training needs analysis for a retail management team. Using the performance feedback provided, identify the top 3 training priorities for the [TEAM] team at [STORE_NAME] (review period: [PERIOD]). For each priority include: (1) skill gap identified, (2) evidence from feedback, (3) business impact if unaddressed (time, cost, or risk), (4) recommended training format (e.g. on-the-job coaching, online module, external course), (5) estimated effort to address in hours. Format: 3 numbered priority sections. Maximum 350 words. Tone: objective, evidence-based. Do not include individual employee names — refer to roles only.

Manager Feedback: [MANAGER_FEEDBACK]


#### Intended Workflow or Task
L&D coordinator inputs quarterly manager feedback for each team. AI generates training priorities summary. HR Manager and L&D lead review and validate. Output submitted to GM People and Culture with budget request attached for approval.

#### Problem Being Solved
2 hours per store per quarter across 40 stores equals 320 hours per year of manual synthesis. Poorly targeted training wastes 10–15% of the L&D budget on low-impact interventions each year — a significant cost given tight retail margins.

#### Automation Potential
**High** — estimated 75% time reduction in synthesis phase (2 hours → ~30 min review). Business impact framing makes output suitable for direct budget submission without further rewriting. Anonymisation protects individual staff data throughout.

#### Risks and Limitations
- **Input Quality Risk:** AI can only analyse the feedback provided — if manager feedback is vague or biased, training recommendations will be too. *Mitigation: HR standardises manager feedback forms to ensure structured, evidence-based input before the prompt is run.*
- **Privacy:** Manager feedback may contain identifiable information about individual staff. *Mitigation: Anonymisation instruction mandated in prompt; outputs stored in secure HR drive and never distributed beyond the HR and L&D team.*

---

## Audit Log

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No data input, no structure | Generic training topics; no relevance to real team needs | Must provide real performance data as input |
| v1.1 | Added RACE role, structured input, justification requirement | Useful output but lacked business impact framing for exec use | Add business impact language for executive audience |
| v1.2 | Business impact per priority, format spec, effort estimate, anonymisation | GM used output directly for budget approval in first quarter | Decision-ready framing unlocks senior leadership use |
