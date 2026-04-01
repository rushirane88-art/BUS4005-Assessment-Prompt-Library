# Prompt 09 — Leave Request Response: Manager Communication

**Business Field:** Retail HR Operations  
**Workflow Task:** Operational HR — Rostering and Leave Communication  
**Current Version:** v1.2 

---

## Version History

### v1.0 — Initial Draft

#### Prompt Text

Write a message about a leave conflict.


#### Intended Workflow or Task
Operational HR — communicating rostering decisions, approved leave, and declined leave requests to retail store staff.

#### Problem Being Solved
Store managers spend approximately 15 minutes per leave conflict communication. With 800 staff across 40 stores, hundreds of these messages are sent monthly across the business.

#### Automation Potential
Very low — vague, impersonal output with no policy context or empathy framing whatsoever.

#### Risks and Limitations
Impersonal messages increase staff dissatisfaction and contribute to voluntary turnover. Blunt decline messages risk damaging the manager-staff relationship and creating avoidable grievances.

---

### v1.1 — Added Empathy Framing and Policy Reference

**What changed:** Added RACE role framing, structured decision input (approved/declined), empathy tone instruction, and a policy reference requirement.  
**Observed effect:** Tone improved significantly and policy reference added credibility. However, message was too long and too formal for the messaging channels actually used by store staff (Microsoft Teams, WhatsApp).  
**Lesson learned:** Channel matters significantly — shorten and adapt format for mobile messaging context.

#### Prompt Text

You are a retail store manager. Write a professional, empathetic message to [EMPLOYEE_NAME] explaining that their leave request for [DATES] has been [approved/declined] because [REASON]. Reference the company leave policy.


#### Intended Workflow or Task
Manager inputs leave decision details. AI drafts message. Manager sends directly or with minor personalisation via Teams or WhatsApp.

#### Problem Being Solved
Hundreds of leave conflict messages monthly across 40 stores. Poor communication quality drives avoidable grievances and is a consistent contributor to voluntary turnover rates.

#### Automation Potential
Medium — tone and policy reference improved significantly but format unsuitable for mobile messaging apps used in real store environments.

#### Risks and Limitations
Format too formal for the context. Retail staff communicate via mobile messaging apps, not formal letters. Risk of message being ignored or perceived as impersonal and bureaucratic.

---

### v1.2 — Final Version 

**What changed:** Added 80-word cap, mobile messaging format instruction, removed policy jargon, added invitation to discuss further.  
**Observed effect:** Piloted across 5 stores. Staff satisfaction with leave communication increased 24% in monthly pulse survey. Manager adoption rate significantly higher due to reduced editing time.  
**Lesson learned:** Channel-appropriate format (mobile, short, warm) is as important as content quality for driving real-world adoption.

#### Prompt Text

You are a retail store manager. Write a brief, professional and empathetic message to [EMPLOYEE_NAME] about their leave request for [DATES]. Decision: [APPROVED or DECLINED]. If declined, reason: [BRIEF_REASON]. If approved, include confirmation and any conditions attached. Tone: warm, direct, respectful. Format: suitable for a team messaging app such as Microsoft Teams or WhatsApp — conversational, maximum 80 words. Do not include policy jargon, legal language, or references to disciplinary consequences. End with an invitation to discuss further if needed.


#### Intended Workflow or Task
Manager selects decision type (approved/declined), inputs dates and reason into the prompt template. AI generates message in under 10 seconds. Manager sends via Teams or WhatsApp with one review and minimal editing. Total time approximately 2 minutes versus 15 minutes for manual drafting.

#### Problem Being Solved
Hundreds of leave messages monthly across 40 stores. Poor communication quality is consistently rated a top-5 dissatisfaction driver in exit interview data — contributing directly to the 55% annual turnover rate. Each turnover event costs an estimated $3,000–$6,000 to replace.

#### Automation Potential
**High** — estimated 85%+ time reduction per message (15 min → ~2 min). Empathy and tone consistency reduces staff grievances across all stores. Channel-appropriate format ensures messages are actually read and responded to rather than ignored.

#### Risks and Limitations
- **Depersonalisation:** Staff may sense AI-generated messages if tone becomes too uniform across all managers. *Mitigation: Managers encouraged to add one personal sentence before sending; brief training provided on personalisation.*
- **Accuracy:** Manager must ensure dates and reason are correct before sending — AI cannot verify HRIS data or current roster. *Mitigation: Manager reviews all variable fields carefully before hitting send; checklist included in training.*

---

## Audit Log

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No context, no tone guidance | Blunt, impersonal output likely to cause grievances | Empathy framing is essential for sensitive staff communications |
| v1.1 | Added empathy framing, policy reference, structured input | Better tone; format too formal for mobile messaging channels | Channel shapes format requirements significantly |
| v1.2 | 80-word cap, mobile format, policy jargon removed, discussion invitation | Staff satisfaction +24% in pilot pulse survey; high manager adoption | Channel-appropriate brevity increases real-world adoption |
