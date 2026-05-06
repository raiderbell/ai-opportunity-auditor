# Reference Audit: Boutique Orthodontic/Prosthodontic Practice
### Sanitized Case Study | Healthcare-Adjacent SMB | AI Opportunity Audit

> **Sanitization note:** All identifying information has been removed. Client name, location, personnel names, and specific financial figures have been generalized or altered. This case study is provided as a reference pattern only.

---

## Business Profile

**Type:** Single-location specialty dental practice (prosthodontics / comprehensive restorative)
**Size:** 1 primary provider + 2–3 hygienists/clinical staff + 1–2 admin staff
**Revenue stage:** Established; $1M+ annual production; modest upward trend
**Ownership:** Solo provider-owner; key-person dependent
**Current advisory engagement:** Growth strategy and DSO partnership evaluation

---

## 1. Current-State Stack Inventory

| Function | Tool / Method | Notes |
|---|---|---|
| Practice management / scheduling | Dedicated dental PM software | Functional; production and collections reports available |
| Billing / insurance | In-house via PM software | Multiple payer types accepted; collections rate strong |
| Patient communication | Weave (dental-specific platform) | Used for payments, some messaging |
| Patient financing | Cherry + CareCredit | Active; indicates operational maturity |
| Bookkeeping / accounting | External CPA | P&L not consistently reviewed by owner |
| HR / payroll | Third-party payroll | Functional |
| Referral tracking | None identified | Referral sources not systematically tracked |
| CRM / recall system | PM software recall module | Functional for existing patients; no external pipeline tracking |

**Stack assessment:** This practice is better-tooled than most at its revenue level. The PM software handles the deterministic layer (scheduling, billing, production reporting) adequately. The gap is in the automation and AI layers — specifically, outbound patient engagement, referral pipeline development, and financial visibility for the owner. The practice is not under-tooled; it is under-utilized.

---

## 2. Workflow Mapping: Highest-Friction Areas

**Workflow A: Large case follow-up**
The practice closes a meaningful volume of large comprehensive cases ($5,000–$50,000+). After treatment planning presentations, follow-up with undecided patients is inconsistent. There is no structured follow-up sequence. The provider handles these personally when time allows.

**Workflow B: Referral source development**
The practice receives referrals from general dentists but does not systematically track which referral sources are most productive or actively nurture those relationships. Business development is passive.

**Workflow C: Owner financial visibility**
The practice produces clean data (production and collections reports are available and reconcilable) but the owner does not review monthly financials at a meaningful level of detail. Decisions are made without a consistent view of overhead, EBITDA, or trend lines.

**Workflow D: Patient recall and reactivation**
The PM software has recall functionality, but reactivation of patients who have lapsed (6–18 months without contact) is not systematically pursued. The practice is leaving re-engagement revenue on the table.

---

## 3. Opportunity Table

| Opportunity | Layer | Impact | Feasibility | Score | Notes |
|---|---|---|---|---|---|
| Large case follow-up sequence | Automation + AI | 5 | 4 | 20 | Automation layer: trigger follow-up sequence when treatment plan is presented but not accepted. AI layer: draft personalized follow-up message based on case type and patient notes. ⚠ Ensure no PHI transmitted through non-HIPAA-compliant tools. |
| Referral source tracking and outreach | Traditional Tools + AI | 4 | 4 | 16 | Track referral sources in a simple spreadsheet or CRM. AI drafts thank-you notes and periodic referral relationship touches for the provider to review and send. |
| Monthly financial summary for owner | Traditional Tools | 4 | 4 | 16 | Not an AI task. Build a one-page dashboard in Excel or Google Sheets pulling from existing PM software reports. The data exists — it just isn't being surfaced. |
| Patient reactivation campaign | Automation + AI | 3 | 4 | 12 | Export lapsed patient list from PM software. AI drafts reactivation message sequence. Automation sends via Weave or email. ⚠ HIPAA flag — confirm patient communication platform is HIPAA-compliant. |
| Provider voice / patient education content | AI | 3 | 5 | 15 | AI drafts patient education content (what to expect from full-arch restoration, implant care, etc.) in the provider's voice. No PHI involved. Immediately usable. |
| Financial reporting analysis | AI | 2 | 3 | 6 | Low priority. The reporting gap is a tooling gap, not a judgment gap. Fix the dashboard first. AI analysis of financial trends is not needed until the owner has a consistent read on the numbers. |

---

## 4. Do Not Automate List

- **Treatment plan presentations.** The provider's clinical credibility and relationship with the patient drive large case acceptance. This is the highest-value human interaction in the practice. Do not automate it, abbreviate it, or delegate it to a system.
- **Post-procedure care follow-up for complex cases.** Full-arch restorations and implant cases have real clinical recovery considerations. Follow-up for these patients should be human, personal, and documented in the chart — not handled by a drip sequence.
- **Insurance disputes and collections calls.** These require judgment, negotiation, and documentation. Rule-based reminders (automation layer) are appropriate; actual dispute conversations are not.
- **Any AI tool that touches PHI.** This practice processes meaningful personal health data. Before deploying any AI tool in a patient-facing workflow, the tool must be evaluated for HIPAA compliance. When in doubt, keep PHI in the PM software and use AI only on de-identified or operational content.

---

## 5. Recommended First Move

**Build a large case follow-up system — automation layer first, AI layer second.**

The practice is producing $1M+ annually with strong collections, which means the revenue engine is working. The highest-leverage opportunity is capturing the large cases that were treatment-planned but not closed. A structured follow-up sequence — even a simple one — directly addresses lost revenue that is already in the pipeline.

Implementation sequence:
1. Identify all treatment plans presented but not accepted in the past 90 days (this is a PM software report — no AI needed).
2. Draft a three-touch follow-up sequence using AI: a warm check-in, a financing reminder, and a final scheduling nudge. Provider reviews and personalizes before sending.
3. Set a recurring monthly reminder (automation) to run the same pull and repeat the sequence for new non-accepted treatment plans.

**Time to implement:** 2–4 hours. No new software required if Weave or email is already in use.

---

*Classification: Sanitized reference case — internal use only. Do not distribute with client-identifying information restored.*
