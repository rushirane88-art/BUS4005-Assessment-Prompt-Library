# Prompt 04 — HR Policy Summary: Plain English Translation

**Business Field:** Retail HR Operations  
**Workflow Task:** Compliance Communication  
**Current Version:** v1.2 

---

## Version History

### v1.0 — Initial Draft

#### Prompt Text

Summarise this HR policy.


#### Intended Workflow or Task
Compliance communication — translating legal policy documents into staff-facing plain-English summaries for distribution.

#### Problem Being Solved
HR team spends approximately 3 hours per policy translating complex legal language. With 20+ active policies updated annually, this totals 60+ hours per year of specialist HR time.

#### Automation Potential
Very low — no audience specification, no reading level guidance, no output structure provided.

#### Risks and Limitations
AI may misrepresent legal obligations without guardrails. Output is a legal paraphrase entirely unsuitable for frontline retail staff with varying literacy levels.

---

### v1.1 — Added Audience Context and RACE Framework

**What changed:** Added RACE role framing, audience specification (frontline retail staff), and 3 required output sections.  
**Observed effect:** Output significantly more readable. However inconsistent structure across runs and one version omitted the disclaimer and 'what to do' section entirely.  
**Lesson learned:** Compliance content requires a mandatory disclaimer and all sections must be explicitly numbered.

#### Prompt Text

You are an HR communications specialist. Summarise the following HR policy in plain English for frontline retail staff who may not have formal HR knowledge. Policy text: [POLICY_TEXT]. Include: what it means for employees, key rules, and what to do if unsure.


#### Intended Workflow or Task
HR compliance officer inputs policy text. Output reviewed by HR manager and legal team before distribution to all store staff.

#### Problem Being Solved
HR team spends approximately 3 hours per policy update translating legal text. With 20+ policies reviewed annually, this is 60+ hours per year of specialist time spent on a drafting task.

#### Automation Potential
Medium — improved readability but variable structure and missing mandatory disclaimer and clear next-step instruction.

#### Risks and Limitations
AI may simplify to the point of misrepresenting legal obligations. Legal review still required in all cases. One output version omitted the 'what to do' section entirely — creating a compliance gap.

---

### v1.2 — Final Version 

**What changed:** Added Year 10 reading level specification, mandatory disclaimer, no-fabrication instruction, and 250-word cap.  
**Observed effect:** Legal team approved format for use. First 3 policies summarised and distributed with zero staff queries about clarity.  
**Lesson learned:** Disclaimers and fabrication-prevention instructions are non-negotiable for all compliance content.

#### Prompt Text

You are an HR communications specialist writing for frontline retail employees at Year 10 reading level. Using the policy text provided, write a plain-English summary with these sections: (1) What this policy is about (2 sentences), (2) What it means for you as an employee (4 bullet points), (3) Key rules to know (3 bullet points), (4) What to do if you have questions (2 sentences, refer to HR team). End with this disclaimer: "This summary is a guide only. Refer to the full policy document for complete details." Maximum 250 words. Do not add information not present in the source policy.

Policy Text: [POLICY_TEXT]


#### Intended Workflow or Task
HR compliance officer provides policy text as input. AI generates draft summary. HR manager and legal counsel review before distribution. Updated automatically whenever the source policy changes.

#### Problem Being Solved
HR team spends approximately 3 hours per policy translating legal language. At 20+ policy updates per year, this is 60+ hours — 1.5 FTE weeks annually on a single communication task.

#### Automation Potential
**High** — estimated 80% time reduction per policy (3 hours → ~35 min for legal review). Legal review retained as mandatory step. Template enforces disclaimer, preventing staff from treating summary as definitive legal guidance.

#### Risks and Limitations
- **Misrepresentation Risk:** AI may oversimplify or omit key legal obligations. *Mitigation: Mandatory legal review before distribution; disclaimer included in every output by template.*
- **Hallucination:** AI instructed not to add information beyond source text, but may still infer incorrectly. *Mitigation: HR manager cross-checks output against source document paragraph by paragraph.*

---

## Audit Log

| Version | Change Made | Observed Effect | Lesson Learned |
|---------|-------------|-----------------|----------------|
| v1.0 | No audience, format, or guardrails specified | Legal paraphrase; unusable for frontline staff | Specify audience reading level and output structure |
| v1.1 | Added audience context, RACE role, 3 sections | More readable but inconsistent; missing disclaimer | Compliance content requires a mandatory disclaimer |
| v1.2 | Reading level, disclaimer, no-fabrication clause, word cap | Legal team approved; distributed to staff successfully | Explicit constraints protect legal compliance |
