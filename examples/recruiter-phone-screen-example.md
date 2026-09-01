# Fictional Example — Senior Software Engineering Manager

This synthetic example demonstrates the interview-plan stage without using real candidate data.

## Role summary

A cloud infrastructure company needs a Senior Software Engineering Manager to lead two backend teams building highly available distributed services. The role requires system-design depth, incident leadership, coaching managers and senior engineers, cross-functional delivery, and responsible adoption of AI-assisted engineering tools.

## Resume summary

Jordan Lee is an Engineering Manager at Northstar Cloud. The resume states that Jordan led 14 engineers, migrated a monolith to services, improved availability from 99.5% to 99.95%, and reduced deployment time by 40%. It mentions hiring six engineers and piloting an AI coding assistant, but gives little detail on architecture tradeoffs, measurement, or AI governance.

## Sample interview plan

### Question 1 — Distributed systems and reliability

- **Question:** Walk me through the most consequential architectural decision you made during the migration from the monolith. What constraints and failure modes did you consider, what tradeoffs did you make, and how did you know the new design improved reliability?
- **Why it matters:** The role requires enough technical depth to lead teams operating highly available distributed services.
- **Evidence prompting it:** The resume claims a service migration and availability improvement but does not explain Jordan's ownership or the causal link.
- **Follow-up probes:**
  1. What would you change if traffic increased tenfold?
  2. Tell me about a failure or incident that challenged the design.
- **Rubric:**
  - **Insufficient:** Cannot describe a specific decision, personal role, constraints, or measurable outcome.
  - **Developing:** Describes the architecture at a high level but offers limited tradeoff analysis or reliability evidence.
  - **Strong:** Clearly explains ownership, alternatives, distributed-system tradeoffs, failure handling, metrics, and lessons learned.
  - **Exceptional:** Meets Strong and shows second-order thinking about scale, operability, organizational constraints, and how evidence changed the design.
- **Positive signals:** Clear ownership boundaries, alternatives considered, reliability metrics, incident learning.
- **Red flags:** Uses team outcomes as personal ownership without clarity; attributes availability gains without evidence.

### Question 2 — Leadership and delivery

- **Question:** Tell me about the deployment-time improvement. How did you determine the bottleneck, align the team and partners, and ensure speed did not reduce quality or reliability?
- **Why it matters:** The role requires cross-functional execution and sustainable engineering leadership.
- **Evidence prompting it:** The resume reports a 40% improvement but does not describe the baseline, intervention, or safeguards.
- **Follow-up probes:**
  1. What resistance did you encounter?
  2. Which leading and lagging indicators did you monitor?
- **Rubric:**
  - **Insufficient:** Provides no specific actions, stakeholders, or credible measurement.
  - **Developing:** Describes actions and a result but lacks baseline, tradeoffs, or leadership detail.
  - **Strong:** Explains diagnosis, influence, execution, safeguards, and verified impact.
  - **Exceptional:** Meets Strong and demonstrates durable mechanisms, organizational learning, and results sustained over time.
- **Positive signals:** Specific baseline, causal reasoning, quality guardrails, shared ownership.
- **Red flags:** Speed presented without quality measures; vague attribution.

### Question 3 — AI fluency and judgment

- **Question:** You mention piloting an AI coding assistant. What problem were you solving, how did you evaluate its impact and risks, and what rules or review mechanisms did you put in place before expanding its use?
- **Why it matters:** The role needs practical AI fluency alongside security, quality, and human judgment.
- **Evidence prompting it:** The resume names an AI pilot but provides no adoption, evaluation, or governance details.
- **Follow-up probes:**
  1. What data would convince you to stop or change the pilot?
  2. How did you address code security, privacy, and overreliance?
- **Rubric:**
  - **Insufficient:** Describes casual tool use without a business problem, evaluation, or risk controls.
  - **Developing:** Identifies a use case and basic benefits but has limited measurement or governance.
  - **Strong:** Connects use to a clear problem, defines success measures, validates output, and implements proportionate safeguards.
  - **Exceptional:** Meets Strong and shows experimentation discipline, stakeholder alignment, adoption strategy, risk monitoring, and evidence-based iteration.
- **Positive signals:** Measured outcomes, human review, privacy/security awareness, willingness to stop.
- **Red flags:** Treats generated output as inherently correct; ignores sensitive code or data risks.
