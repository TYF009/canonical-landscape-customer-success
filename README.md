# Canonical Landscape SaaS — Customer Success Case Study

**Independent hands-on evaluation | Ubuntu device management | Customer onboarding | Customer Success**

This repository documents my independent evaluation of **Canonical Landscape SaaS** from the perspective of a first-time Ubuntu administrator and a prospective Customer Success Manager (CSM).

I configured an Ubuntu virtual machine, connected it to Landscape SaaS and Ubuntu Pro, tested remote administration capabilities, investigated onboarding friction, and developed customer support playbooks and a proposed cross-functional issue-resolution SOP.

> **Scope and attribution:** This is a personal portfolio project, not an official Canonical project or a record of employment at Canonical. The business review presentation uses a **simulated internal CSM reporting scenario**. Findings reflect one test environment and should not be interpreted as validated product defects or enterprise-wide performance results.

## Start here

| Deliverable | What it covers | View | Source file |
| --- | --- | --- | --- |
| **First-Time User Experience & Customer Success Response Strategy** | Detailed testing methodology, evidence, UX observations, CSM response playbooks, and recommendations | [Read report (PDF)](report/Landscape-UX-CSM-Report.pdf) | [Word](report/Landscape-UX-CSM-Report.docx) |
| **Customer Success Business Review** | Executive-style summary of validated outcomes, customer risks, support workflows, cross-functional SOP, and next steps | [View slides (PDF)](presentation/Landscape-CSM-Business-Review.pdf) | [PowerPoint](presentation/Landscape-CSM-Business-Review.pptx) |

## Project overview

**Environment**
- Ubuntu 24.04.4 LTS on VMware
- Canonical Landscape SaaS
- Ubuntu Pro free personal subscription
- One managed Ubuntu instance

**Objectives**
1. Validate the onboarding journey from device registration to the first successful remote task.
2. Test core remote administration capabilities and verify their outcomes locally.
3. Identify friction points that could slow customer adoption or increase support effort.
4. Propose practical CSM responses, escalation paths, and reusable enablement materials.

## Validated outcomes

| Area | Outcome |
| --- | --- |
| Device onboarding | Managed Ubuntu instance registered and appeared **Online** |
| Remote scripting | Script execution succeeded after resolving plugin and authorized-user prerequisites |
| Package management | Installed and removed `cbonsai 1.3.1-1`, with local verification |
| Remote reboot | Reboot request succeeded; instance subsequently returned **Online** |
| Ubuntu Pro visibility | Service states in Landscape matched local `pro status` output |
| Security issues view | Page returned **No security issues found** in this test environment; vulnerability remediation was not tested |

The recorded activity history included **four successful tasks** (script execution, package installation, package removal, and reboot) and **two earlier failed script attempts** that were resolved through configuration and permission changes.

## Key customer-experience observations

| Observation | Evidence level | CSM perspective |
| --- | --- | --- |
| Installation and removal submissions lacked clearly perceived immediate feedback | Repeated first-user observation | Help customers locate Activities, explain asynchronous task states, and propose clearer task confirmations |
| First-time script execution required additional client configuration and an authorized user | Reproduced and resolved | Provide a prerequisite checklist, safe troubleshooting steps, and validation guidance |
| Processes page displayed **No processes running** on an online instance | Observed; root cause unverified | Collect diagnostics, assess impact, and coordinate support investigation without prematurely declaring a defect |
| `dpkg` displayed **Security upgrade** despite matching locally installed and candidate versions | Observed; interpretation unresolved | Clarify status semantics and investigate synchronization or classification as appropriate |

## Proposed Customer Success operating model

The report and presentation outline a reusable issue-handling approach:

**Customer reports an issue → CSM assesses business impact → Evidence and reproduction steps are collected → Technical Support investigates or provides a workaround → Product/Engineering is engaged when appropriate → CSM validates the customer outcome and updates enablement materials.**

Recommended success measures include **Time to First Value (TTFV)**, onboarding completion, remote-task completion, self-service resolution, support-ticket trends, and feature adoption. These are proposed measures—not measured enterprise outcomes from this single-device test.

## Limitations

This was a **single-instance exploratory evaluation** using a personal Ubuntu Pro subscription. It did not involve production customer environments, enterprise-scale deployments, real Canonical support engagements, or statistically representative usability testing. Unresolved behaviors are described as observations requiring further investigation.

## Repository contents

```text
.
├── README.md
├── report/
│   ├── Landscape-UX-CSM-Report.pdf
│   └── Landscape-UX-CSM-Report.docx
└── presentation/
    ├── Landscape-CSM-Business-Review.pdf
    └── Landscape-CSM-Business-Review.pptx
```

*This repository is an independent professional portfolio project and is not affiliated with or endorsed by Canonical.*
