# Prompt 07 — Disciplinary Letter: First Written Warning

**Business Field:** Retail HR Operations  
**Workflow Task:** Performance and Conduct Management  
**Current Version:** v1.2 

---

## Version History

### v1.0 — Initial Draft

#### Prompt Text

Write a first warning letter for an employee.


#### Intended Workflow or Task
Formal HR documentation for performance or conduct management processes when informal discussion has not resolved the issue.

#### Problem Being Solved
HR coordinators spend approximately 90 minutes per disciplinary letter ensuring legal compliance. Errors or omissions in these letters risk unfair dismissal claims at the Fair Work Commission.

#### Automation Potential
Very low — no facts, no legal framework, potentially dangerous output. Not suitable for use in any form without complete rewrite.

#### Risks and Limitations
AI may generate a legally non-compliant letter. High legal exposure. Output would not withstand Fair Work Commission scrutiny if challenged. Using this output without significant legal review would be negligent.

---

### v1.1 — Added Incident Input and Right of Response

**What changed:** Added RACE role framing, structured incident input, right of response requirement, and a meeting offer.  
**Observed effect:** Better structure and legal framing achieved. However, HR manager flagged missing Fair Work Act reference and no mandatory multi-level review instruction — critical for documents of this sensitivity.  
**Lesson learned:** Must reference specific legislative framework and add mandatory human approval step before any letter is issued.

#### Prompt Text

You are an HR advisor. Draft a formal first written warning letter for [EMPLOYEE_NAME] ([JOB_TITLE]) at [STORE_NAME] regarding the following incident: [INCIDENT_SUMMARY]. Reference the relevant company policy. Include the right of response and a meeting to discuss.


#### Intended Workflow or Task
HR coordinator provides incident summary. Draft reviewed by HR manager before issue. Employee meeting arranged before letter is finalised and issued.

#### Problem Being Solved
Approximately 90 minutes per letter for HR coordinators. Average 50 disciplinary letters per year equals 75 hours of high-stakes documentation work requiring specialist knowledge.

#### Automation Potential
Medium — improved legal framing but no explicit Fair Work Act 2009 reference and no mandatory multi-level review instruction built into the output.

#### Risks and Limitations
Without Fair Work Act compliance language, letter may be challenged at the Fair Work Commission. AI may misinterpret the severity of the incident based on the summary provided. No draft watermark means letter could be used prematurely.

---

### v1.2 — Final Version 

**What changed:** Added Fair Work Act 2009 compliance requirement, mandatory DRAFT watermark, multi-level sign-off note, right of response with 5-business-day timeline, and support person entitlement.  
**Observed effect:** First 5 pilot letters reviewed by an external employment lawyer — all cleared as compliant frameworks. Sign-off workflow approved by GM People and Culture.  
**Lesson learned:** Draft watermarks and mandatory multi-level sign-off are essential governance controls for high-stakes legal documents.

#### Prompt Text

You are an experienced Australian HR advisor. Draft a formal first written warning letter compliant with the Fair Work Act 2009. Details — Employee: [EMPLOYEE_NAME], Role: [JOB_TITLE], Store: [STORE_NAME], Date of Incident: [DATE], Incident Summary: [INCIDENT_SUMMARY], Relevant Policy Breached: [POLICY_NAME]. The letter must include: (1) factual account of the incident, (2) specific policy or code of conduct clause breached, (3) expected standard of behaviour going forward, (4) consequences of further breach, (5) employee's right to respond in writing within 5 business days, (6) offer of a follow-up meeting with a support person present. Professional, formal tone. Maximum 400 words. Do not include salary, health information, or personal details unrelated to the incident. End the letter with: "DRAFT — Requires HR Manager and Legal sign-off before issue."


#### Intended Workflow or Task
HR coordinator drafts using AI after incident is documented and investigation notes are complete. HR Manager reviews and approves content. Legal sign-off obtained for complex or senior-level cases. Employee receives letter with formal meeting invitation. Employee response period of 5 business days before any further action is taken.

#### Problem Being Solved
50 disciplinary letters per year at 90 minutes each equals 75 hours of high-stakes drafting. Errors or omissions risk unfair dismissal claims averaging $15,000–$40,000 in Fair Work Commission proceedings — significantly exceeding the cost of the AI solution.

#### Automation Potential
**Medium** — AI drafts only; final sign-off mandatory at all times. Reduces coordinator drafting time by approximately 65% (90 min → ~32 min). DRAFT watermark prevents premature issue before legal review is complete.

#### Risks and Limitations
- **Legal Risk (Highest Sensitivity):** This is the highest legal-risk prompt in the library. *Mitigation: Mandatory DRAFT watermark on every output; HR Manager and Legal sign-off required before issue; AI output is a starting point only — never a final document.*
- **Factual Accuracy:** AI may mischaracterise the severity or nature of the breach based on the incident summary alone. *Mitigation: HR coordinator cross-checks every factual claim in the draft against the original incident report before sign-off.*
- **Over-reliance:** Risk of HR treating the AI draft as near-final and skipping thorough review. *Mitigation: Mandatory sign-off workflow documented in HR procedures; all staff trained on process before access granted.*

---

## Audit Log

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No legal framing, no incident facts provided | Non-compliant letter; legally dangerous to use | High-stakes documents need an explicit legal framework |
| v1.1 | Added RACE role, incident input, right of response | Better structure; Fair Work Act reference missing | Cite specific legislation; add mandatory approval step |
| v1.2 | FWA compliance, DRAFT watermark, sign-off requirement, support person right | External lawyer cleared all 5 pilot letters as compliant | DRAFT watermarks prevent premature use of legal documents |
