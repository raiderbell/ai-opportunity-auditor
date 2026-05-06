# AI Opportunity Auditor
### A folder-based Claude specialist for healthcare-adjacent SMB operations

Add the files in this folder to a Claude Project. Claude becomes an AI Opportunity Auditor — a specialist that tells healthcare-adjacent small businesses exactly where AI will help, where automation is the right call, and where the answer is a better spreadsheet.

---

## What This Is

Most small healthcare businesses have the same conversation about AI: someone reads an article, buys a tool, and six months later the tool is abandoned because it didn't fit the workflow. The problem isn't the tool — it's the missing audit step.

This specialist runs that audit. It applies the 60/30/10 framework from Jake Van Clief's Clief Notes vault to map every task in a business to the right layer: traditional tools, automation, or AI. Then it produces a single output — a Prioritized AI Opportunity Memo — that tells the operator what to do first and why.

**Domain:** Dental practices, dental labs, orthodontic offices, optometry clinics, physical therapy practices, medical spas, and similar owner-operated healthcare businesses with 2–50 employees.

Healthcare is the deliberate constraint. These businesses operate under HIPAA, navigate payer mix complexity, and run provider-dependent revenue models — all of which change which AI tools are appropriate and which carry unacceptable risk. A generic SMB auditor doesn't account for that. This one does.

---

## How to Use It

**This specialist is designed for Claude Projects (claude.ai/projects).** It does not currently work in Cowork mode — Cowork does not pull Project Knowledge files, so the specialist context will not load.

**Step 1.** Go to [claude.ai](https://claude.ai) and create a new Project.

**Step 2.** Open the Project Knowledge panel and upload each file individually. Claude Projects does not accept folders — you must add the five files one at a time:
- `identity.md`
- `rules.md`
- `examples.md`
- `reference/audit-dental-lab.md`
- `reference/audit-orthodontist.md`

**Step 3.** Start a conversation inside the Project. Tell Claude about the business you want audited. You can be brief — the specialist will ask follow-up questions if it needs more information.

That's it.

---

## The 5-Minute Test

A cold tester should be able to do this:

1. Open the Claude Project.
2. Type: *"I run a 4-person dental office. We use Dentrix for scheduling. My office manager spends 3 hours a week on insurance authorizations and I write my own notes. We have no CRM. What should I be using AI for?"*
3. Receive a usable Prioritized AI Opportunity Memo — with a clear first move — in one response.

If that doesn't work, the folder isn't set up correctly.

**Want to probe harder?** Use this more complex prompt:

*"I run a 3-location physical therapy group — 22 employees total, mix of in-network and cash-pay patients. We're on WebPT. Billing is in-house. We do about $2.4M/year but margins are compressing. I have a front desk coordinator, two billing staff, and six therapists. My biggest headaches are: (1) insurance auth denials on initial evals, (2) patients dropping off after 3–4 visits before completing their plan of care, and (3) I have no idea which referral sources are actually sending us cases that close. What should we be doing with AI?"*

A well-configured specialist will triage across all three pain points, assign each to the correct layer, and surface a ranked first move — not just apply AI to everything.

---

## What You Get

Every audit produces one output: a **Prioritized AI Opportunity Memo** with four sections:

1. **Current-State Stack Inventory** — what the business is running today, mapped by function
2. **Opportunity Table** — every identified opportunity, scored by impact and feasibility, layer-assigned
3. **Do Not Automate List** — tasks that should stay human, with plain-language reasons
4. **Recommended First Move** — the single highest-confidence, lowest-risk place to start

The Memo is designed to be handed to an office manager. If the reader has to ask a follow-up question to know what to do next, the Memo isn't done.

---

## Folder Map

```
ai-opportunity-auditor/
├── README.md          ← You are here. Start here.
├── identity.md        ← Who the specialist is and what it does
├── rules.md           ← The 60/30/10 doctrine, the three-question decision test, audit protocol
├── examples.md        ← Annotated example Memo + what good looks like
└── reference/
    ├── audit-dental-lab.md       ← Sanitized reference audit: dental laboratory
    └── audit-orthodontist.md     ← Sanitized reference audit: specialty dental practice
```

---

## The Governing Principle

From Constraint 06 of the Clief Notes vault-toolkit:

> *"The question is not 'can AI do this?' It almost always can. The question is 'should AI do this, or is there a layer beneath AI that handles it better, faster, and cheaper?'"*

This specialist runs that question — systematically, across every workflow a healthcare SMB touches — and gives the operator a ranked answer.

---

## Notes for Healthcare Businesses

This specialist will flag HIPAA/compliance considerations when they arise. It is not a legal resource. Before deploying any AI tool in a patient-facing workflow or any workflow that involves protected health information, consult a healthcare compliance officer or healthcare attorney. The flag in the Memo is a prompt to do that — not a clearance to proceed.

---

*Built on the 60/30/10 framework — Jake Van Clief, Clief Notes.*
*Reference audits are sanitized composites. No client-identifying information is included.*
