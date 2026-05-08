# Reference Audit: Physical Therapy Group (Multi-Location)
### Sanitized Case Study | Healthcare-Adjacent SMB | AI Opportunity Audit

> **Sanitization note:** All identifying information has been removed. Client name, location, personnel names, and specific financial figures have been generalized or altered. This case study is provided as a reference pattern only.

---

## Business Profile

**Type:** Outpatient physical therapy group (3 locations)
**Size:** 22 employees — 6 therapists, 3 PTAs, 4 front desk, 2 billing staff, 1 practice manager, owner
**Revenue stage:** ~$2.4M/year; margins compressing due to payer mix shift and rising overhead
**Ownership:** Solo owner-operator; provider-dependent revenue model
**Payer mix:** ~60% in-network insurance, ~40% cash-pay/direct access

---

## 1. Current-State Stack Inventory

| Function | Tool / Method | Notes |
|---|---|---|
| Scheduling / documentation | WebPT | Functional; documentation and scheduling integrated |
| Billing | In-house via WebPT | 2 dedicated billing staff; auth denial rate elevated |
| Patient communication | Ad hoc (phone + WebPT messaging) | No structured recall or dropout-prevention workflow |
| Bookkeeping / accounting | External CPA | Monthly review; owner not reviewing financials consistently |
| HR / payroll | Third-party payroll | Functional |
| CRM / referral tracking | None | Referral sources not tracked; BD is passive |
| Reporting and KPIs | WebPT reports + manual | Data exists; not surfaced consistently to owner |

**Stack assessment:** Reasonably tooled at the PM layer. The gaps are in the automation and AI layers — specifically around patient retention, referral pipeline development, and financial visibility. Three distinct pain points, three different layer solutions.

---

## 2. Workflow Mapping: Highest-Friction Areas

**Workflow A: Insurance authorization denials on initial evaluations**
Certain payers require prior auth for initial evals on specific CPT codes. When auth is missed or denied, claims are rejected post-service. Billing staff spend significant time on denial follow-up. The rule set (which payers require auth for which codes) is known but not enforced systematically at intake.

**Workflow B: Patient dropout after 3–4 visits**
Patients frequently discontinue before completing their plan of care. Front desk has no structured protocol for reaching out to lapsed patients. Therapists flag it verbally but there is no system-triggered follow-up. Revenue impact is direct — incomplete plans of care reduce visit volume without reducing overhead.

**Workflow C: Referral source tracking**
Most new patients are referred by 4–6 orthopedic surgeons and PCPs. No CRM exists. The owner cannot identify which referral sources are sending high-value cases (those that complete care) vs. low-retention referrals. BD is entirely passive.

**Workflow D: Owner financial visibility**
WebPT produces production and collections reports. The owner does not review them consistently. Decisions are made without a reliable read on location-level P&L, payer mix contribution, or therapist utilization rates.

---

## 3. Opportunity Table

| Opportunity | Layer | Impact | Feasibility | Score | Notes |
|---|---|---|---|---|---|
| Insurance auth pre-screening at intake | Automation | 5 | 4 | **20** | If payer + CPT code → flag for auth before scheduling. Rule table, not judgment. Test 2 yes. Build in WebPT workflow or intake form logic. |
| Patient dropout outreach | Automation + AI | 4 | 4 | **16** | Automation: trigger outreach when patient misses visit or goes 7 days without scheduling. AI: draft the outreach message with appropriate tone for the case type. ⚠ Confirm messaging platform is HIPAA-compliant. |
| Referral source tracking | Traditional Tools | 4 | 4 | **16** | Simple CRM (HubSpot free or Airtable) tracks referral source per patient, case outcome, completion rate. Test 1 yes — deterministic. No AI. |
| AI-drafted referral relationship touches | AI | 3 | 5 | **15** | Once referral sources are tracked, AI drafts periodic thank-you notes and case update summaries for the owner to review and send. No PHI in the outreach. |
| Location-level financial dashboard | Traditional Tools | 4 | 3 | **12** | WebPT data + Excel or Google Sheets. One-page monthly view: production, collections, utilization by location. Not an AI task — data exists, just not surfaced. |
| Auth denial appeal drafts | AI | 3 | 3 | **9** | AI can draft appeal letters using denial reason codes and clinical notes. Moderate feasibility — requires clean process for feeding denial data to the tool. ⚠ PHI involved — HIPAA-compliant tool required. Lower priority until auth pre-screening reduces denial volume first. |

---

## 4. Do Not Automate

- **Initial evaluation and plan of care presentation:** The therapeutic relationship and patient buy-in to the plan are established here. This is the highest-value human interaction in the practice. Shortening or systematizing it to save time will increase dropout — the exact problem the practice is trying to solve.
- **Provider-to-provider referral conversations:** Orthopedic surgeons refer based on relationships and outcomes. These calls and visits must be personal. AI can draft the prep materials; the owner makes the call.
- **Clinical decision-making on plan of care modifications:** When a patient is plateauing or showing complications, the therapist decides. No automation in the clinical loop.
- **Insurance dispute calls:** Denial appeals that require verbal negotiation with payer representatives stay human. AI drafts the written appeals; billing staff makes the calls.
- **Any patient communication tool that hasn't been evaluated for HIPAA compliance:** The practice touches PHI in virtually every patient interaction. Vet the tool before deploying it.

---

## 5. Recommended First Move

**Implement auth pre-screening at intake — automation layer, no AI required.**

The highest-leverage opportunity is not AI — it's stopping the auth denial problem before it starts. The rule set already exists (which payers require auth for which CPT codes). The problem is it's not enforced at the point of scheduling. Build a simple decision table — in WebPT intake workflow, an intake form, or even a laminated desk reference — that flags auth-required cases before the appointment is booked.

This is a one-time build with compounding payoff: fewer denials means less billing staff time on appeals, faster collections, and cleaner payer data to analyze later.

**First AI move (parallel, low-effort):** Draft a 3-message dropout outreach sequence using AI — a check-in, a scheduling nudge, and a care reminder. Have the practice manager review and approve the templates. Wire them to the scheduling trigger once confirmed. This costs one afternoon and directly addresses the dropout problem.

---

*Classification: Sanitized reference case — internal use only. Do not distribute with client-identifying information restored.*
