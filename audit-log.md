# Audit Log — Full Iteration History

**Subject:** BUS4005 Assessment 1  
**Business Field:** Retail HR Operations  

This file documents the complete iteration audit trail for all 10 prompts. Each entry shows what changed at each version, the observed effect on output quality, and the lesson learned.

---

## Prompt 01 — Welcome Email: New Hire Onboarding

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | Initial — broad instruction only | Output generic; unusable without full rewrite | Need role framing and output structure |
| v1.1 | Added RACE role + 4 section headings | Better tone; variable length (400+ words) | Add explicit word limit and format constraints |
| v1.2 | Word limit (220) + exclusions + numbered structure | Consistent, business-ready output in 9 min review | Format constraints = reliable, deployable outputs |

---

## Prompt 02 — Job Advertisement: Retail Vacancy

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | Minimal — role name only | Vague generic output; no legal elements | Role specs and tone constraints are essential |
| v1.1 | Added RACE role and 3 sections | Better structure; no EEO clause or salary field | Legal requirements must be made explicit |
| v1.2 | Added EEO, salary field, word cap (350), section structure | Compliance-ready output; 15 min review sufficient | Mandate all legal and format requirements in prompt |

---

## Prompt 03 — Performance Review Summary

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No input data, no structure | Meaningless generic output; completely unusable | Performance prompts need real data as input |
| v1.1 | Added RACE, structured notes input, rating section | Usable draft but rating section flagged as risky | Remove AI from rating decisions entirely |
| v1.2 | Removed rating, added privacy exclusions, word cap (280) | HR-approved; used successfully in 12 pilot reviews | AI drafts, humans decide on sensitive matters |

---

## Prompt 04 — HR Policy Summary: Plain English

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No audience, format, or guardrails specified | Legal paraphrase; unusable for frontline staff | Specify audience reading level and output structure |
| v1.1 | Added audience context, RACE role, 3 sections | More readable but inconsistent; missing disclaimer | Compliance content requires a mandatory disclaimer |
| v1.2 | Year 10 reading level, disclaimer, no-fabrication clause, word cap (250) | Legal team approved; distributed to staff successfully | Explicit constraints protect legal compliance |

---

## Prompt 05 — Structured Interview Question Set

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | Generic — no role, structure, or competency map | 12 generic questions; no competency alignment | Competency mapping and role context are essential |
| v1.1 | Added RACE role and behavioural/situational framing | Better structure; one legally sensitive question generated | Must add explicit EEO exclusion list to prompt |
| v1.2 | Legal exclusions, STAR framing, competency tags, word cap (400) | Legal-approved; 18% interview score improvement in pilot | Legal safeguards must be built directly into the prompt |

---

## Prompt 06 — Exit Interview Summary Report

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No input data provided | AI fabricated departure reasons entirely | Must provide actual interview notes as input |
| v1.1 | Added structured input and 3 output sections | Useful summaries; identifying details retained in aggregate | Anonymisation and escalation flags are necessary |
| v1.2 | Anonymisation, escalation flag, neutral tone, word cap (200) | 3 escalation cases identified in pilot; HR Manager approved | Risk-detection features transform summaries into governance tools |

---

## Prompt 07 — Disciplinary Letter: First Written Warning

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No legal framing, no incident facts provided | Non-compliant letter; legally dangerous to use | High-stakes documents need an explicit legal framework |
| v1.1 | Added RACE role, incident input, right of response | Better structure; Fair Work Act reference missing | Cite specific legislation; add mandatory approval step |
| v1.2 | FWA 2009 compliance, DRAFT watermark, sign-off requirement, support person right | External lawyer cleared all 5 pilot letters as compliant | DRAFT watermarks prevent premature use of legal documents |

---

## Prompt 08 — Training Needs Analysis Summary

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No data input, no structure | Generic training topics; no relevance to real team needs | Must provide real performance data as input |
| v1.1 | Added RACE role, structured input, justification requirement | Useful output; lacked business impact framing for exec use | Add business impact language for executive audience |
| v1.2 | Business impact per priority, format spec, effort estimate, anonymisation | GM used output directly for budget approval in Q1 | Decision-ready framing unlocks senior leadership adoption |

---

## Prompt 09 — Leave Request Response

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No context, no tone guidance | Blunt, impersonal output likely to cause grievances | Empathy framing is essential for sensitive staff communications |
| v1.1 | Added empathy framing, policy reference, structured input | Better tone; format too formal for mobile messaging channels | Channel shapes format requirements significantly |
| v1.2 | 80-word cap, mobile format, policy jargon removed, discussion invitation | Staff satisfaction +24% in pilot pulse survey | Channel-appropriate brevity increases real-world adoption |

---

## Prompt 10 — Recruitment Pipeline Status Report

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No data input provided | AI fabricated entire pipeline — completely unusable | Reports always need real structured data as input |
| v1.1 | Added structured ATS data input and 3 report sections | Functional output; missing exec summary and status indicators | Management needs a scannable visual format for quick decisions |
| v1.2 | Executive summary, status labels, priority action owners, privacy exclusion | Adopted as standard by GM; 2 critical vacancies escalated in week 1 | Visual status indicators drive faster management decisions |

---

## Cross-Prompt Patterns and Key Insights

**1. RACE Framework (Role, Action, Context, Execute)**  
Applied to all prompts from v1.1 onwards. Consistent finding: adding a clear role (e.g. "You are an HR onboarding specialist") significantly improved tone, relevance, and structure in every case.

**2. Output Constraints Are Not Optional**  
Word limits, section numbering, and format specifications were the single biggest differentiator between v1.1 (medium automation) and v1.2 (high automation). Unconstrained prompts produce variable, unreliable outputs.

**3. Legal and Privacy Exclusions Must Be Explicit**  
"Do not include..." instructions were critical for prompts 01, 02, 03, 04, 06, 07, 09, and 10. AI cannot infer what to exclude — it must be told explicitly.

**4. High-Stakes Documents Need Multiple Controls**  
Prompt 07 (Disciplinary Letter) required the most controls: FWA compliance reference, DRAFT watermark, multi-level sign-off, and right of response. Single safeguards are not sufficient for legal documents.

**5. Channel-Appropriate Format Matters for Adoption**  
Prompt 09 demonstrated that even a well-written message will not be used if the format doesn't match the actual communication channel. 80-word mobile format drove 24% satisfaction improvement vs. formal letter format.

**6. Business Impact Framing Unlocks Executive Use**  
Prompt 08 showed that adding business impact language (cost, time, risk) to AI output transforms it from a useful internal tool into a board-ready document — enabling faster decisions without additional analyst work.
