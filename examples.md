# EXAMPLES: What a Good Memo Looks Like

This file contains one annotated example of a complete Prioritized AI Opportunity Memo. Use it to calibrate output quality and format.

For full reference audits from real engagements, see:
- `reference/audit-dental-lab.md`
- `reference/audit-orthodontist.md`

---

## Example Memo: Physical Therapy Practice, 6 Employees

**Input provided by operator:**
> "We run a small PT practice — 6 people total, 3 therapists, 2 front desk, and me. We're on WebPT for scheduling and documentation. Billing goes through a third-party biller. I spend probably 4 hours a week on insurance authorizations and another 2–3 hours on writing progress notes. We have no CRM. Referrals come mostly from 4 orthopedic surgeons and we never follow up with them systematically. Revenue is around $850K/year. I want to know where AI can actually help."

---

## PRIORITIZED AI OPPORTUNITY MEMO

**Business:** Physical therapy practice (6 employees, $850K revenue)
**Date of audit:** [Date]
**Prepared by:** AI Opportunity Auditor

---

### Recommended First Move

**AI-assisted progress note drafting.**

You are spending 2–3 hours per week writing progress notes — documentation that has a consistent structure, domain-specific language, and low variability in format. This is a high-feasibility AI task: a well-structured prompt in a HIPAA-compliant tool (verify your vendor) can reduce note drafting time by 50–70% for therapists who dictate or take brief session notes. At 3 therapists spending similar time, this recovers 6–9 hours of clinical capacity per week. That is the highest-impact, highest-feasibility item in this audit.

**⚠ HIPAA/Compliance flag:** Progress notes contain PHI. Any AI tool used for this workflow must be evaluated for HIPAA compliance. Do not use consumer AI tools (ChatGPT, Claude.ai standard) for identifiable patient documentation. Consult your compliance officer before implementation.

---

### 1. Current-State Stack Inventory

| Function | Tool | Status |
|---|---|---|
| Scheduling / documentation | WebPT | Functional |
| Billing | Third-party biller | Functional |
| Insurance authorizations | Manual (owner-led) | 4 hrs/week — friction identified |
| Progress notes | Manual (all therapists) | 2–3 hrs/week each — friction identified |
| Patient communication | Unknown / ad hoc | Gap — no system identified |
| Referral tracking / CRM | None | Gap |
| Financial reporting | Unknown | Not described |

---

### 2. Opportunity Table

| Opportunity | Layer | Impact | Feasibility | Score |
|---|---|---|---|---|
| AI-assisted progress note drafting | AI | 5 | 4 | **20** |
| Referral relationship outreach (surgeon touches) | AI | 4 | 5 | **20** |
| Insurance authorization status tracking | Traditional Tools | 4 | 4 | **16** |
| Automated patient recall / appointment reminders | Automation | 3 | 5 | **15** |
| Insurance auth pre-screening (if/then rules) | Automation | 3 | 3 | **9** |
| Financial reporting dashboard | Traditional Tools | 3 | 3 | **9** |

**Notes on layer assignments:**

- **Progress note drafting (AI):** Requires synthesis of session observations into structured clinical language. Test 3 is a yes.
- **Referral outreach (AI):** Drafting personalized communication to 4 orthopedic relationships — tone, context, timing all matter. Test 3 is a yes. No PHI involved.
- **Authorization tracking (Traditional Tools):** This is a lookup and status-tracking problem. A shared spreadsheet or a simple Airtable base with status fields handles this better than AI. Test 1 is a yes — stop there.
- **Patient reminders (Automation):** If patient hasn't confirmed appointment within 48 hours → send reminder. This is an if/then rule. Test 2 is a yes.
- **Auth pre-screening (Automation):** Certain payers require auth for certain CPT codes — a rule table, not a judgment call. Test 2 is a yes.
- **Financial reporting (Traditional Tools):** The data exists in the billing system. Build a monthly one-page dashboard. No AI needed.

---

### 3. Do Not Automate

- **Initial patient evaluations.** The therapeutic relationship starts here. The human interaction is the product.
- **Any documentation workflow using non-HIPAA-compliant AI.** The regulatory exposure is not worth the time savings.
- **Referral conversations with surgeons.** Relationship-built referral pipelines depend on personal contact. AI can draft the content; the therapist sends it.
- **Collections calls and insurance disputes.** These require judgment, negotiation, and documentation. Rule-based reminders (automation) are fine; conversations are not.

---

---

## ✦ CALIBRATION NOTES — For Specialist Reference Only
### What makes this Memo work (not part of any deliverable)

---

**1. It leads with the first move.** The practice owner knows what to do before reading the table.

**2. The table is honest about layers.** Four of the six items are not AI — they are traditional tools or automation. This is what the 60/30/10 framework produces when applied correctly. If every item in the table says "AI," the audit is wrong.

**3. HIPAA flags are explicit, not buried.** Healthcare businesses need to see compliance considerations called out clearly, not woven into fine print.

**4. The do-not-automate list is specific.** It is not generic advice about "keeping humans in the loop." It names the actual workflows this practice should not automate and why.

**5. It is short.** A practice owner with six employees and $850K in revenue does not need a 20-page strategy document. They need to know what to do Monday morning.
