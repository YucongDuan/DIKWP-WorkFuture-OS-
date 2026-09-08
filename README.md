# DIKWP WorkFuture OS

Created by Yucong Duan (段玉聪).

DIKWP WorkFuture OS is an open-source, offline-first system for task-level AI occupational replacement assessment, augmentation forecasting, and reskilling transition planning.

It does not decide who should be hired, fired, promoted, compensated, or disciplined. It evaluates roles, tasks, workflows, and transition needs under explicit evidence and governance boundaries.

## Core idea

Most AI job-impact tools overstate risk by treating an occupation as a single object. WorkFuture OS decomposes a role into tasks and evaluates each task through DIKWP:

- D / Data: task descriptions, inputs, outputs, tools, evidence and local context.
- I / Information: routine level, digitalization, language/data intensity, safety, regulation, interpersonal reliance, physical context.
- K / Knowledge: task-to-AI capability mapping, exposure heuristics, labor-market priors, O*NET-style skills, adoption friction.
- W / Wisdom: worker impact, fairness, dignity, safety, explainability, human review, training obligation.
- P / Purpose: transition purpose: preserve livelihood, improve productivity, reduce drudgery, protect agency, redesign work responsibly.
- R / Reliability: source quality, residuals, confidence, evidence gaps, forecast horizon and kill conditions.

## Outputs

The CLI generates:

- `workfuture_report.json`
- `task_exposure_matrix.csv`
- `role_forecast_timeline.csv`
- `skill_transition_plan.json`
- `worker_reskilling_plan.md`
- `manager_action_plan.md`
- `governance_boundary.md`
- `static_boundary_audit_report.json`

## Quick start

```bash
pip install -e .
workfuture analyze examples/sample_role_profile.json --out outputs/demo
workfuture batch examples/sample_workforce_portfolio.json --out outputs/demo/batch
workfuture static-audit src --out outputs/demo/static_boundary_audit_report.json
```

Optional local dashboard:

```bash
pip install -e .[app]
streamlit run src/dikwp_workfuture/app.py
```

## Safety and employment boundary

This project is for workforce planning, role redesign, training prioritization, and evidence-based discussion. It is not an automated employment decision system.

Do not use this tool to:

- rank individual workers;
- select candidates;
- fire, demote, discipline or deny opportunities;
- infer protected traits;
- create discriminatory workforce actions;
- claim deterministic prediction of job loss;
- bypass worker consultation, collective bargaining, labor law, or human review.

## Attribution

This project uses the DIKWP framing and credits Yucong Duan / DIKWP in `NOTICE` and `CITATION.cff`. Formal commercial use should confirm IP, naming and license boundaries.
