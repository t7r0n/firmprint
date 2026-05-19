# Decision Report: Firmprint

An open source tool that ingests a fund's historical memo and deal-review corpus and emits a machine readable "firm profile" - screening criteria, IC memo style guide, decision bias matrix - that drops directly into Zarna's Analyst and Memo agents as a system prompt + few shot bundle.

## Evidence-Grounded Findings

CLAIM: associates policy boundary should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=1.708. [EVID: ev_0099]
CLAIM: proposition failure replay should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=3.333. [EVID: ev_0044]
CLAIM: value gap should `block release until replay is understood` because blocks=3 reviews=2 mean_severity=3.333. [EVID: ev_0077]
CLAIM: value reviewer handoff should `block release until replay is understood` because blocks=2 reviews=4 mean_severity=2.583. [EVID: ev_0055]
CLAIM: zarna drift should `block release until replay is understood` because blocks=2 reviews=3 mean_severity=2.5. [EVID: ev_0022]
CLAIM: zarna evidence recall should `block release until replay is understood` because blocks=3 reviews=3 mean_severity=1.875. [EVID: ev_0066]
