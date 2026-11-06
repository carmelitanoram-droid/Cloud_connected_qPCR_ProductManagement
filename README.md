# Cloud-Connected qPCR: Product Management & Workflow Analytics

**An evidence-led product management case study using simulated customer feedback and qPCR platform telemetry.**

This portfolio project investigates workflow friction in a fictional cloud-connected quantitative PCR (qPCR) platform. It demonstrates how customer feedback can guide telemetry analysis, how findings translate into product priorities, and how a prioritized opportunity becomes actionable requirements and a proposed roadmap.

## Product context

The fictional platform supports qPCR experiment configuration, cloud synchronization, remote monitoring, LIMS export, and audit report workflows. Its stakeholders include bench scientists, assay developers, lab managers, quality teams, and IT/data administrators.

**Product question:** Which workflow improvements should be addressed first, and what evidence supports that decision?

## Investigation approach

Customer feedback was categorized by product module and severity. The four investigation areas were reviewed in descending order of **Critical + High feedback share**:

| Investigation order | Area | Critical + High feedback |
| --- | --- | ---: |
| 1 | Audit & Traceability | 32/48 (66.7%) |
| 2 | Data Export & Integration | 28/43 (65.1%) |
| 3 | Cloud Sync | 16/25 (64.0%) |
| 4 | Experiment Setup | 16/39 (41.0%) |

Telemetry was then examined at the appropriate event, session, and account levels. The dataset includes **48 simulated customer accounts**.

## Key findings

| Workflow | Observed result | Product opportunity |
| --- | --- | --- |
| Audit report export | 15/105 export attempts failed (14.3%); 11 accounts affected | Improve export reliability and retry |
| LIMS export | 27/277 attempts failed (9.7%); 17 accounts affected | Improve export error handling and retry |
| Cloud synchronization | 26 accounts affected; 28 recovered sessions and 5 with no recorded completion; median normal/recovered durations: 72/756 seconds | Reduce recovery delays and improve failure guidance |
| Experiment setup | 457 sessions reopened; 46 accounts affected | Guided setup and consolidated pre-run review |

## Product Insights Dashboard

The Excel dashboard summarizes customer problem prevalence, telemetry evidence, and RICE-based feature prioritization, supporting the proposed product roadmap.

![Cloud-connected qPCR Product Insights Dashboard](dashboard/qPCR_dashboard_preview.png)
 

**Interpretation caution:** A reopened setup session does not necessarily represent avoidable rework. Longer recovered synchronization sessions do not isolate the time attributable solely to retries.

## Product prioritization

Five evidence-supported feature candidates were compared using **RICE** (Reach × Impact × Confidence ÷ Effort). Reach was approximated using distinct affected accounts; the other inputs are provisional product-planning estimates.

| Rank | Feature | RICE score |
| ---: | --- | ---: |
| 1 | Guided experiment setup | 24.53 |
| 2 | Cloud-sync recovery | 18.72 |
| 3 | Sync-failure notifications | 14.56 |
| 4 | LIMS export reliability | 14.45 |
| 5 | Audit report export reliability | 10.69 |

The full backlog contains 12 features; seven additional candidates remain in discovery and were not assigned artificial scores.

## Delivery proposal

The highest-ranked feature, **Guided Experiment Setup**, was developed into two user stories:

1. **Guided qPCR experiment configuration:** assay template selection, visual plate-map assignments, and retained settings across setup steps.
2. **Pre-run configuration review:** a consolidated review screen, targeted editing, and validation of required settings before starting a run.

Both stories have testable acceptance criteria and a shared proposed Definition of Done in the case study.

**Proposed roadmap:** Phase 1 — setup usability; Phase 2 — sync recovery and failure guidance; Phase 3 — LIMS and audit export reliability. These are proposed outcomes, not committed releases.

## Repository contents

| Path | Contents |
| --- | --- |
| [`report/`](report/) | Five-page product management case study (PDF) |
| [`analysis/`](analysis/) | Master Excel workbook: customer feedback, telemetry, pivots, backlog, RICE, user stories, roadmap and data dictionary |
| [`dashboard/`](dashboard/) | Excel product-insights dashboard |

**Suggested reading order:** Read the report first, view the dashboard second, then explore the supporting workbook. The workbook's worksheet names are referenced in the report for traceability.

## Tools and skills demonstrated

Microsoft Excel, pivot tables, workflow telemetry analysis, problem framing, customer feedback triage, RICE prioritization, user stories, acceptance criteria, Definition of Done, and outcome-based roadmapping.

## Data and limitations

All customer accounts, product events, and performance measurements are **synthetic and created for portfolio demonstration**. The analysis describes observed patterns in that simulated dataset; it does not establish causal relationships or demonstrate realized product improvements. RICE inputs and roadmap phases require validation with product stakeholders and engineering teams.
