# Firmprint

An open source tool that ingests a fund's historical memo and deal-review corpus and emits a machine readable "firm profile" - screening criteria, IC memo style guide, decision bias matrix - that drops directly into Zarna's Analyst and Memo agents as a system prompt + few shot bundle.

## Why This Exists

Zarna's value proposition is "AI associates tuned to your firm's evaluation methods, decision making patterns, and institutional knowledge" (zarnaai.com). Their go to market is forward deployed engineering - embedding with a fund for weeks to elicit the firm's screening rubric, IC template, and CRM taxonomy, then encoding that into the four associates. That elicitation is the bottleneck.

## What It Builds

- Replays synthetic `zarna` and `value` cases against the project's evidence rules.
- Scores `zarna_coverage`, `value_risk`, and `proposition_precision` so regressions are visible in CSV and JSON.
- Plants `zarna drift` and `value gap` failures as negative controls.
- Writes citation-locked decision claims; unsupported claims fail verification.
- Exports a review dashboard and demo pack for `firmprint` without hosted services.

## Local Run

```bash
uv sync
uv run firmprint all
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/analysis.json`
- `outputs/scenario_report.csv`
- `outputs/decision_report.md`
- `outputs/evidence_packet.md`
- `outputs/domain_rubric.json`
- `outputs/failure_matrix.md`
- `outputs/trace_graph.mmd`
- `outputs/dashboard.html`
- `outputs/demo_pack.zip`

## Sources

- https://www.ycombinator.com/companies/zarna
- https://www.linkedin.com/posts/rishabh-dhariwal_grateful-to-share-that-zarna-yc-f25-is-activity-7376677228031455232-v64j
- https://www.zarnaai.com/team/rishabh
- https://www.crunchbase.com/person/vivan-agrawal
- https://www.crunchbase.com/person/rakesh-mehta-bd61
- https://www.crunchbase.com/organization/zarna
- https://www.alternates.ai/finance-and-operations/agent/zarna

## Boundary

This repository uses synthetic fixtures only. It has no credentials, no customer data, no outreach data, and no dependency on a hosted API.
