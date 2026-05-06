# Reference Audit: Regional Dental Lab
### Sanitized Case Study | Healthcare-Adjacent SMB | AI Opportunity Audit

> **Sanitization note:** All identifying information has been removed. Client name, location, personnel names, and specific financial figures have been generalized or altered. This case study is provided as a reference pattern only.

---

## Business Profile

**Type:** Independent dental laboratory (B2B — serves dentist offices, not patients directly)
**Size:** 8–12 employees, two operating locations being consolidated into one
**Revenue stage:** Established; pursuing expansion to a second metro market
**Ownership:** Partnership; one active managing partner, one passive partner
**Current advisory engagement:** Fractional COO/CRO support for growth and capital strategy

---

## 1. Current-State Stack Inventory

| Function | Tool / Method | Notes |
|---|---|---|
| Case tracking | Manual log + email | No dedicated lab management software in place |
| Invoicing / billing | QuickBooks | In use but inconsistent; bookkeeping had been managed internally by a non-specialist |
| Client communication | Phone + email, ad hoc | No CRM; relationships are personal and untracked |
| Scheduling / production | Whiteboard + verbal | No digital production scheduling |
| HR / payroll | Third-party payroll service | Functional |
| Financial reporting | QuickBooks + manual | Bookkeeping cleanup required before any reporting is meaningful |
| Business development | Relationship-driven, no system | Owner handles all BD personally |

**Stack assessment:** This business is operating primarily on Layer 1 (traditional tools) in theory, but in practice is under-tooled even for that layer. Several functions that should be handled by deterministic systems (case tracking, invoicing reconciliation, financial reporting) are instead handled manually or inconsistently. Before AI is introduced, the baseline systems need to be stabilized.

---

## 2. Workflow Mapping: Highest-Friction Areas

**Workflow A: Case intake and tracking**
Cases arrive via phone or email from dentist offices. A staff member logs them manually. There is no system-of-record for case status, turnaround time, or delivery confirmation. Cases occasionally fall through the cracks. Owner visibility into production pipeline is limited to what staff reports verbally.

**Workflow B: Invoicing and collections**
Invoices are generated in QuickBooks but follow-up on aging accounts receivable is inconsistent. There is no automated reminder sequence. The owner is the primary collection point of contact.

**Workflow C: Business development**
All new client relationships are initiated and maintained by the managing partner. No referral tracking, no outreach cadence, no CRM. The business is dependent on a single person for all revenue growth.

**Workflow D: Financial visibility**
Books require cleanup from a prior period of informal bookkeeping. Monthly financials are not consistently reviewed. The owner cannot currently produce a reliable P&L on demand.

---

## 3. Opportunity Table

| Opportunity | Layer | Impact | Feasibility | Score | Notes |
|---|---|---|---|---|---|
| Accounts receivable follow-up reminders | Automation | 4 | 4 | 16 | Trigger-based email/SMS sequence for aging invoices. No AI needed — this is an if/then rule (invoice age > 30 days → send reminder). |
| Case tracking system | Traditional Tools | 5 | 3 | 15 | Lab management software (e.g., LabArchives, or a simple Airtable base) eliminates manual logging. Pure deterministic layer — no AI. |
| Bookkeeping cleanup and monthly reporting | Traditional Tools | 5 | 2 | 10 | Requires a specialist, not AI. Assign to a bookkeeper; use QuickBooks properly. |
| BD outreach drafts (email templates for new dentist prospects) | AI | 3 | 5 | 15 | AI can draft personalized outreach emails based on a practice profile. Low risk, zero HIPAA exposure (B2B), immediately usable. |
| Referral tracking and CRM | Traditional Tools | 4 | 3 | 12 | A simple HubSpot free tier or Airtable base handles this. Rule-based follow-up reminders once CRM is in place. Not an AI task. |
| Client communication summaries (post-call notes) | AI | 2 | 5 | 10 | AI can turn a brief voice memo or rough notes into a formatted call summary. Low priority until higher-impact items are addressed. |

---

## 4. Do Not Automate List

- **Partner negotiation and equity conversations.** The managing partner is navigating a complex partner buyout timeline. These conversations require human judgment, legal counsel, and relationship management. No AI.
- **Capital and funding discussions.** Conversations with lenders and funding facilitators are relationship-dependent and context-sensitive. AI can help prepare for them; it should not conduct them.
- **Client relationship management for existing accounts.** The lab's competitive advantage is personal service. Automating client-facing communication for established accounts risks eroding the relationships that sustain the revenue base.
- **Hiring decisions.** The lab is thin-staffed and adding the wrong person is costly. Keep humans in the loop for all hiring.

---

## 5. Recommended First Move

**Implement a basic case tracking system (Airtable or equivalent) before adding any AI.**

The highest-leverage action is not AI — it is establishing a system-of-record for production. Without it, there is nothing for AI to work with and no way to measure the impact of any improvement. The business development email drafting (AI layer, score 15) is ready to implement immediately in parallel and costs nothing — but the foundational infrastructure comes first.

**First AI move:** Draft a library of 5–7 prospecting email templates in a Claude Project for new dentist outreach. The managing partner provides a brief practice profile; Claude drafts the outreach. This reduces the time cost of BD outreach and builds a repeatable system around what is currently an entirely personal, non-scalable process.

---

*Classification: Sanitized reference case — internal use only. Do not distribute with client-identifying information restored.*
