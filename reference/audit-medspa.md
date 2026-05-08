# Reference Audit: Medical Spa (Aesthetic Practice)
### Sanitized Case Study | Healthcare-Adjacent SMB | AI Opportunity Audit

> **Sanitization note:** All identifying information has been removed. Client name, location, personnel names, and specific financial figures have been generalized or altered. This case study is provided as a reference pattern only.

---

## Business Profile

**Type:** Owner-operated medical spa — injectables, laser treatments, body contouring, skincare
**Size:** 8 employees — 1 medical director (owner), 2 injectors/aestheticians, 2 laser techs, 2 front desk, 1 part-time bookkeeper
**Revenue stage:** ~$1.2M/year; heavily dependent on repeat clients and word-of-mouth referrals
**Ownership:** Solo owner; provider-dependent on the medical director for injectable services
**Payer mix:** Cash-pay only — no insurance. Membership program (monthly retainer) accounts for ~30% of revenue.

---

## 1. Current-State Stack Inventory

**Note on HIPAA scope:** Medical spas occupy a nuanced compliance position. When services are performed under physician supervision and medical records are kept, HIPAA applies. Most of the AI opportunities below involve marketing and client communication — which typically do not involve PHI — but the practice should confirm scope with their compliance advisor before deploying any AI tool that touches client records.

| Function | Tool / Method | Notes |
|---|---|---|
| Scheduling / booking | Vagaro or equivalent spa/med software | Functional; online booking enabled |
| Client records / charting | Paper or basic EMR | Varies; often a gap in this segment |
| Billing / payments | Square or integrated POS | Cash-pay; functional |
| Client communication | Email + text via scheduling platform | Inconsistent; no structured recall sequence |
| Bookkeeping | Part-time bookkeeper + QuickBooks | Functional but owner not reviewing regularly |
| HR / payroll | Third-party payroll | Functional |
| CRM / loyalty tracking | None or basic loyalty module | Membership managed manually or in scheduling software |
| Marketing | Ad hoc (Instagram, occasional email blast) | No content calendar; no systematic follow-up |
| Reporting / KPIs | Scheduling software reports | Data exists; not consistently reviewed |

**Stack assessment:** Lean but functional at the operational layer. The biggest gaps are in client retention infrastructure, marketing systematization, and owner financial visibility. This is a cash-pay business — every lapsed client is pure revenue loss with no insurance backstop. Retention and reactivation are the highest-leverage opportunities.

---

## 2. Workflow Mapping: Highest-Friction Areas

**Workflow A: Client recall and reactivation**
Botox clients need retreatment every 3–4 months. Filler clients every 6–12 months. Laser packages lapse without follow-up. The scheduling platform has a recall module but it's not configured or used consistently. Lapsed clients are not systematically contacted. Front desk handles recall ad hoc when the schedule has gaps.

**Workflow B: Membership management**
~30% of revenue comes from a monthly membership program. Members are tracked manually or in a basic spreadsheet. Membership renewals are not automated. Churn is not tracked. The owner cannot tell which membership tier has the highest retention or lifetime value.

**Workflow C: Social media and content**
The practice posts to Instagram inconsistently. Content is created reactively — photos taken when someone remembers, captions written on the fly. No content calendar. No repurposing of before/after content into email or other channels. The owner knows this is leaving revenue on the table but doesn't have bandwidth to fix it.

**Workflow D: New client follow-up**
After a first visit, new clients receive no structured follow-up sequence. The window for converting a one-time client to a repeat client is highest in the 2 weeks post-visit. This window is not being used.

---

## 3. Opportunity Table

| Opportunity | Layer | Impact | Feasibility | Score | Notes |
|---|---|---|---|---|---|
| Automated recall sequences by treatment type | Automation | 5 | 5 | **25** | Botox at 12 weeks, filler at 6 months, laser package follow-up at 30 days. If/then rule by service type and last visit date. Test 2 yes. Configure in scheduling platform or Zapier. No AI needed. |
| New client follow-up sequence | Automation + AI | 4 | 5 | **20** | Automation: trigger 3-touch sequence at 2 days, 1 week, 2 weeks post first visit. AI: draft the sequence messages in the practice's voice. No PHI in marketing communications. |
| Membership tracking dashboard | Traditional Tools | 4 | 4 | **16** | Airtable or Google Sheets: member tier, join date, renewal date, services used, churn flag. Test 1 yes — deterministic. Adds visibility the owner currently has zero of. |
| Social content calendar and draft generation | AI | 3 | 5 | **15** | AI drafts captions, email copy, and treatment spotlights on a weekly cadence. Owner or injector reviews and posts. No PHI. Immediately usable. High feasibility — no new tools. |
| Lapsed client reactivation campaign | Automation + AI | 4 | 3 | **12** | Export lapsed clients (no visit in 6+ months) from scheduling software. AI drafts personalized reactivation offers. Automation sends via email/SMS. Moderate feasibility — requires clean client data export. |
| Financial reporting dashboard | Traditional Tools | 3 | 4 | **12** | Monthly one-pager: revenue by service line, membership retention rate, avg client value. Data exists in scheduling + QuickBooks. Not an AI task. |
| AI-drafted treatment plan summaries | AI | 2 | 3 | **6** | Post-consultation AI summary of recommended treatment plan for the client to take home. Low priority — charting workflow must be stable first. ⚠ May involve PHI depending on charting setup — confirm HIPAA scope. |

---

## 4. Do Not Automate

- **Consultation and treatment plan presentation:** This is the sale. The injector's expertise, aesthetic eye, and relationship with the client drive conversion on high-ticket services. Systematizing the consultation experience will erode the trust that justifies premium pricing.
- **Before/after photography and consent:** Both require in-person staff involvement and documented client consent. No automation in this workflow.
- **Complaint and adverse event follow-up:** Any client reporting an unexpected reaction or unsatisfactory result must receive a personal call from the medical director. Do not route these through automation.
- **Membership renewal conversations for high-value clients:** Top-tier members who are considering canceling should get a personal call, not an automated drip. The LTV of a retained high-value member far exceeds the cost of the call.
- **Any tool that touches medical records without HIPAA evaluation:** Confirm with your compliance advisor which workflows involve PHI before deploying AI in the clinical documentation layer.

---

## 5. Recommended First Move

**Configure recall sequences by treatment type — automation layer, no AI required.**

The highest-leverage opportunity is also the simplest: the practice is sitting on a recall engine that it hasn't turned on. Botox clients who don't receive a 12-week reminder will book somewhere else or let the habit lapse. This is not a content problem — it's a trigger problem. Configure the scheduling platform's recall module (or a simple Zapier automation if the platform doesn't support it) with three sequences: Botox at 12 weeks, filler at 6 months, laser package follow-up at 30 days.

This requires no AI, no new software, and recovers revenue that is already in the client base.

**First AI move (parallel):** Draft a 3-touch new client follow-up sequence using AI — a thank-you and care instructions at 48 hours, a check-in and rebooking prompt at 1 week, and a treatment recommendation at 2 weeks. The owner or lead injector approves the copy once. Wire it to the first-visit trigger. Done.

---

*Classification: Sanitized reference case — internal use only. Do not distribute with client-identifying information restored.*
