# BUS4005 — Assessment 1: Prompt Library

**Subject:** BUS4005 — AI in Business  
**Assessment:** Assessment 1 — Prompt Library & Consultancy Pitch  
**Business Field:** Retail HR Operations  
**Due:** End of Week 4

---

## Overview

This repository contains the complete prompt library developed for Assessment 1. The library consists of 10 AI prompts designed to automate high-volume, repetitive HR workflows in a mid-size Australian retail business (~800 staff, 40 stores, 55% annual turnover).

Each prompt has been developed through a minimum of 3 iterations (v1.0 → v1.1 → v1.2), with full documentation of what changed, the observed effect, and the lesson learned at each stage.

---

## Business Context

**Organisation:** Mid-size Australian retail chain  
**Problem:** HR team of 6 coordinators spending 60–70% of time on repetitive, text-heavy tasks — leaving little capacity for strategic people work  
**Solution:** 10 targeted AI prompts addressing the highest-volume operational pain points  
**Governance:** Human-in-the-loop retained for all external-facing outputs; AI handles drafts only

---

## Prompt Library — 10 Entries

| # | Prompt | Workflow Area | Final Version |
|---|--------|---------------|---------------|
| 01 | [Welcome Email — New Hire Onboarding](prompts/prompt-01-welcome-email.md) | HR Onboarding | v1.2 ✅ |
| 02 | [Job Advertisement — Retail Vacancy](prompts/prompt-02-job-advertisement.md) | Recruitment | v1.2 ✅ |
| 03 | [Performance Review Summary](prompts/prompt-03-performance-review.md) | Performance Management | v1.2 ✅ |
| 04 | [HR Policy Summary — Plain English](prompts/prompt-04-policy-summary.md) | Compliance Communication | v1.2 ✅ |
| 05 | [Structured Interview Question Set](prompts/prompt-05-interview-questions.md) | Recruitment | v1.2 ✅ |
| 06 | [Exit Interview Summary Report](prompts/prompt-06-exit-interview.md) | Retention Analysis | v1.2 ✅ |
| 07 | [Disciplinary Letter — First Written Warning](prompts/prompt-07-disciplinary-letter.md) | Conduct Management | v1.2 ✅ |
| 08 | [Training Needs Analysis Summary](prompts/prompt-08-training-needs.md) | Learning & Development | v1.2 ✅ |
| 09 | [Leave Request Response](prompts/prompt-09-leave-response.md) | Operational HR | v1.2 ✅ |
| 10 | [Recruitment Pipeline Status Report](prompts/prompt-10-recruitment-report.md) | HR Reporting | v1.2 ✅ |

---

## Each Prompt Entry Contains

1. **Prompt Text** — the exact text tested in the AI system (v1.0, v1.1, v1.2)
2. **Intended Workflow or Task** — where the prompt fits in the HR process
3. **Problem Being Solved** — operational pain point framed in business terms (time, cost, risk)
4. **Automation Potential** — how much AI can handle, and what human oversight remains
5. **Risks and Limitations** — specific risks, business impact, and mitigations

---

## Iteration Evidence

Each prompt file documents:
- What changed at each version
- The observed effect on output quality
- The lesson learned that informed the next iteration

The **commit history** of this repository serves as the primary iteration audit trail. Each commit corresponds to a prompt version update.

---

## Audit Log — Summary

| Prompt | v1.0 Issue | v1.1 Improvement | v1.2 Fix |
|--------|-----------|-----------------|---------|
| 01 Welcome Email | Too generic; full rewrite needed | Added RACE + 4 sections | Word limit + exclusions |
| 02 Job Ad | No legal elements | Added structure | EEO clause + salary field |
| 03 Performance Review | No data input | Added structured notes | Removed rating; privacy exclusions |
| 04 Policy Summary | Legal paraphrase; unreadable | Added audience + sections | Disclaimer + no-fabrication clause |
| 05 Interview Questions | Generic; no competency map | Added STAR + competency | EEO exclusion list added |
| 06 Exit Interview | AI fabricated data | Added structured input | Anonymisation + escalation flag |
| 07 Disciplinary Letter | No legal framework | Added FWA reference | DRAFT watermark + sign-off |
| 08 Training Needs | No data; generic output | Added structured input | Business impact framing added |
| 09 Leave Response | Impersonal; no tone | Added empathy + policy | 80-word cap + mobile format |
| 10 Pipeline Report | AI fabricated pipeline | Added ATS data input | Exec summary + status labels |

---

## Prompting Strategies Used

- **RACE Framework** (Role, Action, Context, Execute) — applied to all prompts from v1.1
- **Output constraints** — word limits, section numbering, format specifications
- **Chaining** — prompts designed as steps in broader HR workflows
- **Legal and privacy exclusions** — explicit "do not include" instructions for sensitive content
- **Escalation triggers** — automated flags for serious disclosures (Prompt 06)
- **Draft watermarks** — mandatory for high-stakes legal documents (Prompt 07)
