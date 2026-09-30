# AI Hiring Funnel Diagnostic

Find where a recruiting process may need attention, check the data behind the numbers, and prepare a useful search-reset conversation.

## What this tool does

This workflow helps a recruiter turn stage counts and process notes into:

- A clear view of stage-to-stage conversion
- Data-quality warnings
- Questions about possible bottlenecks
- A short list of actions for the recruiter and hiring manager
- A follow-up plan to see whether changes helped

The output is a discussion aid. AI does not determine why a candidate left a process or whether an interviewer, recruiter, or candidate was at fault.

## Choose how to provide the funnel information

| Option | What the recruiter provides | What happens |
|---|---|---|
| Manual entry | Completed funnel input template below | The AI assistant organizes the supplied counts and context |
| ATS report upload | An approved, aggregated CSV report and a short explanation of its columns | An AI assistant that supports file uploads reviews column mappings before analysis |
| ATS integration request | ATS name, report or data required, stage definitions, and access requirements | The assistant prepares a connection requirements brief for the company's authorized administrator or implementation team |

This resource is a copy-and-paste AI workflow, not a deployed application or an installed ATS connector. Uploads occur in the employer-approved AI assistant, where supported. Direct ATS retrieval requires a separately implemented and authorized connection. Selecting or naming an ATS does not establish that connection.

### Option 1: Manual entry

Complete the input template below. Write `Unknown` where information is unavailable. Never replace a missing count with an estimate.

### Option 2: Upload an ATS report

1. Export an aggregated report from your ATS or spreadsheet.
2. Remove candidate-level rows, personal identifiers, private notes, and unnecessary columns before uploading.
3. Use an employer-approved AI assistant that permits the report and supports CSV uploads.
4. Tell the assistant which columns mean stage, entered, advanced, still active, and time in stage.
5. Provide the cohort definition, outcome check date, and process context.
6. Review the proposed mapping and data-quality warnings before requesting the diagnostic.

If upload is unavailable, paste the approved aggregate table using the manual-entry option. Do not upload a candidate-level export simply to ask AI to remove personal details afterward.

Example upload instruction:

~~~text
Use the attached approved aggregate CSV as the funnel source.
First list its columns and propose a mapping to the input template.
Do not assume that similar stage labels mean the same thing.
Confirm the cohort and count definitions from the context I supplied.
Flag missing or conflicting fields before analysis.
Do not claim access to any ATS beyond this uploaded file.
~~~

Example aggregate CSV using fictional data:

~~~csv
stage,entered,advanced,still_active,median_days
Recruiter screen,40,20,0,3
Hiring-manager interview,20,10,0,5
Interview loop,10,3,0,8
Offer,3,2,0,4
~~~

For the Offer row, "advanced" means accepted offers. The example describes one completed candidate cohort with outcomes checked at the same cutoff. It is not a live ATS export.

### Option 3: Describe the ATS integration you need

The recruiter can name any ATS and describe the desired integration. The implementation team must check the provider's current official documentation, supported reports, permissions, and company requirements before building it.

~~~text
ATS name:
Desired report or information:
Role, job family, and level filters:
Candidate cohort definition:
Reporting period and outcome cutoff:
Company stage names and intended mapping:
Needed aggregate fields:
Preferred update frequency:
Existing company-approved connector, if known:
Authorized ATS administrator or implementation team:
Approved destination for the report:
Security, retention, and access requirements:
Unknown requirements:
~~~

Use this integration-planning prompt:

~~~text
Help me define an ATS connection for the Hiring Funnel Diagnostic.

[PASTE COMPLETED INTEGRATION REQUIREMENTS]

Prepare:
1. A requirements brief using only supplied facts.
2. Proposed aggregate fields and stage mappings for my review.
3. Missing information the authorized administrator must confirm.
4. A minimum-access, read-only connection proposal.
5. Provider documentation and API capabilities that the implementation team must verify.
6. A validation plan comparing retrieved aggregates with an approved ATS report.
7. Data handling, retention, access, and disconnection requirements requiring approval.

Do not ask me to paste passwords, API keys, or tokens into this conversation.
Do not claim that a connection exists or that you retrieved records unless an authorized integration actually did so.
Do not retrieve data, create credentials, or change ATS records as part of this planning step.
If access to candidate-level records is technically necessary to create aggregates, identify that need for security and privacy review before implementation.
~~~

Once an approved connector has been implemented, its validated aggregate output can feed the same diagnostic prompt. Credentials belong in an approved secure configuration, not in this public repository or a prompt.

## What you need

Use approved, aggregated information for one role or a clearly defined group of comparable roles:

- Role or job family and level
- Reporting period and candidate cohort
- Number of candidates entering each stage
- Number advancing from each stage
- Number still active at each stage
- Median time spent in each stage, if available
- Documented process changes
- Approved, aggregated reason codes, if available
- Hiring-manager and interviewer feedback themes with personal details removed
- Previously agreed goals or benchmarks, if any

Do not paste resumes, interview transcripts, candidate names, employee names, contact information, compensation records, health information, or other personal data. Apply company rules for suppressing small groups that could identify a person.

## Define the cohort first

A funnel is only useful when its counts describe the same group of candidates.

For example, "candidates who entered a recruiter screen during August, with outcomes checked on September 15" is a defined cohort. A table that mixes everyone who was screened in August with everyone who interviewed in August may describe different people. Do not calculate a meaningful conversion rate from those mixed counts.

Record candidates who are still active separately. Their outcomes are not yet known.

## Input template

~~~text
INPUT METHOD
Manual entry / Uploaded aggregate report / Validated authorized connector output:
Source report and extraction date:
Column or stage mappings requiring confirmation:

ROLE AND PERIOD
Role or job family:
Level:
Reporting period:
Candidate cohort definition:
Outcome check date:
Approved goals or benchmarks, if any:

STAGE DATA
Stage 1 name:
Candidates entering:
Candidates advancing:
Candidates still active:
Median days in stage, if known:

Stage 2 name:
Candidates entering:
Candidates advancing:
Candidates still active:
Median days in stage, if known:

[REPEAT FOR EACH STAGE]

PROCESS CONTEXT
Changes during this period:
Documented feedback themes, aggregated:
Approved reason codes, aggregated:
Known scheduling or approval delays:
Known data gaps or conflicting records:
Questions the recruiter wants to answer:
~~~

## Copy-and-paste AI prompt

~~~text
You are helping a recruiter review an aggregated hiring funnel.

Use only the supplied data and context. Do not invent candidate outcomes, reasons for rejection, interviewer behavior, benchmarks, or causes of low conversion. Do not evaluate individual candidates or make hiring decisions.

Source information:
[PASTE THE COMPLETED INPUT TEMPLATE AND/OR REFERENCE THE APPROVED AGGREGATE FILE]

If I supplied an integration request without retrieved data, prepare the integration requirements brief only. Explain that funnel analysis requires actual validated aggregate data.

Create the following:

### 1. Data-quality check

Identify:
- Whether all stage counts belong to the same candidate cohort
- Missing counts, dates, or stage definitions
- Cases where a later-stage count exceeds an earlier-stage count
- Candidates still active whose outcomes are not final
- Changes in the process that make periods hard to compare
- Small sample sizes that make a percentage easy to overinterpret
- Unverified file-column or ATS-stage mappings

If the cohort or denominator is unclear, stop short of calculating a conversion rate for that stage. State what must be verified.

### 2. Funnel table

Where the data supports calculation, create:

| Stage | Entered | Advanced | Still active | Conversion among resolved candidates | Median days | Data caveat |
|---|---:|---:|---:|---:|---:|---|

Only when outcomes are mutually exclusive and fully accounted for:
Resolved = Entered - Still active
Conversion among resolved candidates = Advanced / Resolved × 100

Verify that all counts are non-negative and Advanced does not exceed Resolved. If Resolved is zero, report "Not calculable." Do not silently repair inconsistent data.

Disclose the numerator and denominator for every rate. If candidates are still active, label the rate provisional; faster decisions may differ from later outcomes. Do not treat an in-progress candidate as a rejection. Identify whether "advanced" means stage progression or offer acceptance.

### 3. Observations

Describe up to three notable patterns. For each, separate:
- What the data shows
- What remains unknown
- What information would help explain it

Do not label a pattern "the problem" solely because its percentage is the lowest.

### 4. Possible explanations to investigate

Provide questions, not conclusions. Consider only explanations relevant to the supplied evidence, such as:
- Role or level calibration
- Screening criteria
- Candidate communication
- Scheduling delays
- Interview-plan consistency
- Feedback quality
- Offer timing
- Changes in sourcing mix

For every possible explanation, name the evidence needed to test it and the person or team best placed to verify it.

### 5. Search-reset meeting agenda

Prepare a 20-minute discussion for the recruiter and hiring manager:
1. Confirm the cohort and data quality
2. Review the most useful funnel observations
3. Compare actual evidence with the approved hiring rubric
4. Choose no more than two process changes
5. Assign owners and a review date

### 6. Action plan

Create this table:

| Proposed action | Evidence behind it | Owner | Review date | Measure to watch | Risk or tradeoff |
|---|---|---|---|---|---|

Recommend actions only when their rationale is visible. Label unverified ideas as experiments. Mark unspecified owners or dates "Needs assignment" or "Needs confirmation."

### 7. Leadership summary

Write no more than 120 words explaining:
- What is known
- What needs verification
- What the team agreed to test, if an agreement was supplied
- When results will be reviewed

Do not claim that a process change improved hiring until results have been measured.

### 8. Human-review checklist

Ask the recruiter to confirm:
- All counts and stage definitions match the source system
- The cohort is consistent
- Active candidates are accounted for
- Percentages use disclosed denominators
- No candidate or employee personal data appears
- Hypotheses are not presented as facts
- Proposed changes align with the approved hiring rubric
- The hiring manager owns decisions about the role's evaluation bar

Finish with:
"AI organized the funnel evidence and suggested questions. The recruiter and hiring manager must verify the data, investigate the causes, and decide what to change."
~~~

## Fictional example

A fictional senior infrastructure search has a completed cohort with no candidates still active:

| Stage | Entered | Advanced | Conversion |
|---|---:|---:|---:|
| Recruiter screen | 40 | 20 | 50% |
| Hiring-manager interview | 20 | 10 | 50% |
| Interview loop | 10 | 3 | 30% |
| Offer | 3 | 2 accepted | 67% |

**What the data shows:** Three of ten candidates who entered the interview loop received offers. The loop-to-offer conversion was 30% for this completed cohort. Offer acceptance was 2/3, or approximately 67%.

**What it does not show:** The numbers alone do not explain whether the issue was role calibration, interview design, candidate interest, scheduling, or another factor. Ten interview loops are also a small sample.

**Useful next question:** For this cohort, did the interview loop consistently assess the criteria agreed at intake? The recruiter and hiring manager can review aggregated feedback themes and the approved rubric before changing the process.

**Possible experiment:** If the review finds that interviewers assessed different criteria, clarify ownership of each competency in the interview plan. Review the next completed cohort before claiming an improvement.

All counts, roles, and outcomes in this example are fictional.

## Review guidance

1. Reconcile the counts with the applicant tracking system.
2. Verify file-column mappings and ATS-stage definitions.
3. Check that stage names mean the same thing throughout the reporting period.
4. Keep active candidates separate from completed outcomes.
5. Look at counts alongside percentages, especially with small samples.
6. Ask the hiring manager and relevant interviewers to validate process explanations.
7. Document any changes and review their effect on a later cohort.
8. Keep candidate decisions within the approved, human-led evaluation process.

## Responsible-AI and privacy safeguards

- Use aggregated, de-identified data and apply company small-group reporting rules.
- Remove private data before uploading; aggregation alone does not guarantee anonymity.
- Do not include candidate-level notes, transcripts, resumes, or personal details.
- Do not infer protected characteristics or use demographic proxies.
- Do not ask AI to rate recruiters, interviewers, or candidates from funnel percentages.
- Do not present a correlation as a proven cause.
- Do not invent an external benchmark or treat a generic benchmark as the company's goal.
- Have qualified people verify calculations, context, and proposed changes.
- Use an employer-approved AI system for internal recruiting information.
- Uploading or pasting data into an AI service transmits it to that service; follow approved access and retention rules.
- A future ATS connection must disclose what it retrieves, where processing occurs, and what is retained, and receive company approval before activation.
- Keep credentials out of prompts and public repositories.

## Intended impact

The workflow is designed to help recruiters spot questions worth investigating and lead a more evidence-based search-reset discussion. Any time savings or conversion improvement must be measured; this resource does not guarantee either.

## Disclaimer

This is a recruiting-operations aid, not a validated hiring assessment or an automated employment decision system. Adapt it to approved company processes. The example uses only synthetic data.
