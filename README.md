# Firmprint

An open source tool that ingests a fund's historical memo and deal-review corpus and emits a machine readable "firm profile" — screening criteria, IC memo style guide, decision bias matrix — that drops directly into Firmprint's Analyst and Memo agents as a system prompt + few shot bundle.

![Firmprint working dashboard](outputs/project_working.svg)

## Why it exists

Firmprint's value proposition is "AI associates tuned to your firm's evaluation methods, decision making patterns, and institutional knowledge" (Firmprintai.com). Their go to market is forward deployed engineering — embedding with a fund for weeks to elicit the firm's screening rubric, IC template, and CRM taxonomy, then encoding that into the four associates..

The project is intentionally built as a local replay harness instead of a slide. It creates fixtures, plants realistic failure modes, produces citation-locked evidence, and turns the result into a dashboard a reviewer can inspect without credentials or hosted services.

## What is inside

- Deterministic fixture generation for the company-specific risk surface.
- Strategy code in `src/firmprint/strategy.py` with project-specific scoring and visual evidence.
- Citation-locked reports where every decision claim points to a generated evidence ID.
- Two regenerated visual artifacts: `outputs/project_working.svg` and `outputs/evidence_map.svg`.
- A portable demo pack with JSON, CSV, Markdown, HTML, SVG, benchmark, and test artifacts.

![Firmprint evidence map](outputs/evidence_map.svg)

## Signals it measures

- `Firmprint coverage`
- `value risk`
- `proposition precision`
- `associates latency`

## Failure modes it plants

- Firmprint drift
- value gap
- proposition misroute
- associates blindspot

## Run it locally

```bash
uv sync
uv run firmprint all
uv run pytest -q
uv run ruff check .
```

## Outputs worth opening

- `outputs/dashboard.html`
- `outputs/project_working.svg`
- `outputs/evidence_map.svg`
- `outputs/operator_brief.md`
- `outputs/decision_report.md`
- `outputs/strategy_model.json`
- `outputs/demo_pack.zip`

## Boundary

Everything runs locally against synthetic fixtures. There are no credentials, no customer records, no outreach files, and no hosted API dependency.
