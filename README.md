# AI Recruiting Toolkit

Practical AI workflows for recruiters, recruiting leaders, and Talent Operations teams.

This project applies AI to real recruiting problems without removing human judgment from hiring decisions. The toolkit focuses on clearer intake, stronger personalization, consistent documentation, and more recruiter capacity.

## Why this exists

Recruiters spend significant time turning unstructured conversations and notes into usable information. AI can accelerate that work, but the recruiter must still validate the output, protect candidate information, and own the final decision.

This toolkit is informed by 15+ years of recruiting experience and leadership across technical hiring, infrastructure, cloud, software, data centers, and semiconductor talent.

## Included workflows

| Workflow | Recruiting problem | Output |
|---|---|---|
| [Hiring-manager intake synthesis](prompts/hiring-manager-intake.md) | Intake notes are inconsistent or incomplete | Structured search brief and calibration questions |
| [Candidate outreach generator](prompts/candidate-outreach.md) | Outreach becomes generic at scale | Personalized, evidence-based message |
| [Interview debrief synthesis](prompts/interview-debrief.md) | Feedback is scattered or vague | Competency-aligned summary with gaps flagged |
| [Responsible-AI checklist](governance/responsible-ai-checklist.md) | AI creates privacy, bias, or accuracy risks | Human-review and data-protection controls |

A fictional [sample intake](examples/sample-intake.md) is included so the workflows can be tested without candidate or employer data.

## Recommended workflow

1. Remove confidential, sensitive, and personally identifiable information.
2. Provide the model with the role criteria and relevant source material.
3. Request a structured output with clear evidence boundaries.
4. Review every statement for accuracy and unsupported inference.
5. Apply human judgment before communicating or making a decision.

## What AI should not decide

AI should not independently reject candidates, infer protected characteristics, manufacture candidate qualifications, determine culture fit, or replace structured human evaluation.

## About the author

Matthew Rojas is a Talent Acquisition leader with 15+ years of experience. At AWS, he helped scale a centralized recruiting organization from 3 to approximately 40 recruiters in seven months and reduced recruiter onboarding from eight weeks to four.

## Disclaimer

All examples are fictional and use synthetic data. This repository contains no confidential employer information or real candidate data. Adapt these workflows to your organization's legal, privacy, security, and employment requirements.
