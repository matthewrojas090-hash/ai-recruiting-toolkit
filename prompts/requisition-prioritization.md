# AI Requisition Prioritization Assistant

Turn a crowded list of open roles into a structured recruiting plan while keeping final priority decisions with people.

## What this tool does

This workflow helps recruiting teams:

- Compare open requisitions using consistent criteria
- Identify roles that may need immediate attention
- Surface missing or conflicting information
- Separate business urgency from stakeholder pressure
- Recommend recruiter focus areas for the week
- Create a concise leadership update
- Document the reasoning behind prioritization decisions

AI organizes the information. Recruiting and business leaders remain responsible for final decisions.

## What you need

Prepare factual information for each open requisition:

- Role title
- Department
- Hiring manager
- Date opened
- Target hiring date
- Business impact
- Approved headcount status
- Number of qualified candidates
- Current interview stage
- Known hiring risks
- Recruiter capacity required
- Dependencies or deadlines

Remove candidate names, contact information, compensation details, and confidential business information before using an external AI system.

## Copy-and-paste input template

~~~text
Role title:
Department:
Date opened:
Target hiring date:
Headcount approval: Confirmed / Pending / Unknown
Business impact: Critical / High / Standard / Unclear
Qualified candidates currently active:
Furthest candidate stage:
Time-sensitive deadline or dependency:
Known hiring risks:
Estimated recruiting effort: High / Medium / Low / Unknown
Additional factual context:
~~~

Repeat the template for each requisition.

## Copy-and-paste AI prompt

~~~text
You are assisting a recruiting team with weekly requisition planning.

Use only the information provided below. Do not invent business impact, deadlines, candidate activity, headcount approval, stakeholder commitments, or hiring risks.

Open requisitions:

[PASTE COMPLETED REQUISITION TEMPLATES]

Evaluate each requisition across these dimensions:

1. Business impact
2. Time sensitivity
3. Headcount approval
4. Pipeline health
5. Hiring risk
6. Estimated recruiting effort
7. Age of the requisition
8. Dependencies affecting other teams or commitments

Create the following output:

### 1. Information-quality check

For each requisition, identify missing, unclear, or conflicting information that should be verified before setting priorities.

### 2. Recommended priority groups

Place each requisition into one preliminary group:

- Priority 1: Immediate focus
- Priority 2: Active progress
- Priority 3: Maintain or monitor
- Needs clarification: Insufficient information

Explain the recommendation using only supplied facts. Do not treat stakeholder seniority, repeated escalation, or job title alone as proof of business importance.

### 3. Evidence table

Create a table with these columns:

| Role | Preliminary priority | Supporting facts | Missing information | Primary risk | Recommended next action |

### 4. Capacity risks

Identify where the proposed priorities may exceed available recruiting capacity. Do not assume capacity that was not provided.

### 5. Weekly action plan

Recommend up to five concrete actions for the recruiting team. Distinguish between:

- Recruiter actions
- Hiring-manager actions
- Leadership decisions
- Information that must be verified

### 6. Leadership summary

Write a concise update covering:

- Roles requiring immediate attention
- Roles with healthy progress
- Decisions or support needed
- Important risks
- Information that remains unverified

### 7. Human-review questions

Provide five questions leaders should answer before approving the final priority order.

Finish with this reminder:

“AI produced a preliminary planning recommendation, not a final staffing decision. Validate the facts, consider organizational context, and document any human adjustments.”
~~~

## Optional weighted review

Teams that already use an approved scoring process can ask AI to organize the inputs against these example weights:

| Dimension | Example weight |
|---|---:|
| Business impact | 25% |
| Time sensitivity | 20% |
| Pipeline risk | 15% |
| Approved dependency or commitment | 15% |
| Requisition age | 10% |
| Candidate activity | 10% |
| Recruiting effort | 5% |

These weights are examples only. They should not be adopted without agreement from recruiting and business leadership.

A numeric score can create false confidence when the underlying information is incomplete. Always retain the written evidence and uncertainty notes.

## Fictional example

### Synthetic requisition information

~~~text
Role title: Senior Cloud Engineer
Department: Infrastructure
Date opened: June 15
Target hiring date: September 30
Headcount approval: Confirmed
Business impact: Critical
Qualified candidates currently active: 1
Furthest candidate stage: Recruiter screen
Time-sensitive deadline or dependency: Required for a fictional October platform launch
Known hiring risks: Specialized technical background and limited pipeline
Estimated recruiting effort: High
Additional factual context: Two previous finalists withdrew

Role title: Operations Coordinator
Department: Workplace Operations
Date opened: August 10
Target hiring date: November 1
Headcount approval: Confirmed
Business impact: Standard
Qualified candidates currently active: 8
Furthest candidate stage: Final interviews
Time-sensitive deadline or dependency: None provided
Known hiring risks: None documented
Estimated recruiting effort: Low
Additional factual context: Three final interviews are scheduled

Role title: Product Marketing Manager
Department: Marketing
Date opened: August 18
Target hiring date: Unknown
Headcount approval: Pending
Business impact: High
Qualified candidates currently active: 0
Furthest candidate stage: Not started
Time-sensitive deadline or dependency: Unclear
Known hiring risks: Approval and scope remain unresolved
Estimated recruiting effort: Unknown
Additional factual context: Hiring manager requested immediate sourcing
~~~

### Example preliminary output

| Role | Preliminary priority | Supporting facts | Missing information | Primary risk | Recommended next action |
|---|---|---|---|---|---|
| Senior Cloud Engineer | Priority 1 | Confirmed headcount, critical impact, October dependency, limited pipeline and two withdrawals | Recruiter capacity and revised sourcing plan | Low pipeline for a time-sensitive role | Hold a search reset and expand evidence-based sourcing channels |
| Operations Coordinator | Priority 2 | Confirmed headcount and three scheduled final interviews | Final interview outcomes | Process completion | Maintain candidate communication and complete scheduled interviews |
| Product Marketing Manager | Needs clarification | Hiring manager requested sourcing, but approval is pending | Target date, approved scope, dependency and recruiting effort | Work may begin before the role is authorized | Confirm approval and role requirements before launching a full search |

The example does not automatically place the newest or loudest request first. It distinguishes verified urgency from an unconfirmed request.

## Questions for the weekly prioritization meeting

1. Which business-impact statements have been verified?
2. What deadline or dependency makes each Priority 1 role urgent?
3. Are any searches active without confirmed approval?
4. Which roles have enough pipeline activity to require less sourcing attention?
5. Where does recruiter capacity conflict with the proposed plan?
6. What changed since the previous review?
7. Who owns each decision or next action?

## Responsible-use guidelines

- Do not include candidate names or personal information.
- Do not allow AI to make final hiring or staffing decisions.
- Do not infer importance from a leader’s title or escalation frequency.
- Do not present an AI-generated score as an objective fact.
- Verify business impact, deadlines, and approval status.
- Document human changes to the recommended order.
- Revisit priorities when facts or organizational needs change.
- Keep the process transparent enough for stakeholders to understand.

## Disclaimer

This resource provides a planning framework, not legal, HR, or workforce-planning advice. Every organization should adapt it to its policies, systems, and review requirements. All examples are fictional and use synthetic data.
