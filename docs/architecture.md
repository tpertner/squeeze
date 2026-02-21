# Architecture (at a glance)

    Prompt A (baseline) ────┐
                            ├──> Run both prompts ─> Score with rubric ─> Drift report ─> Regression test
    Prompt B (pressure) ────┘

## What this diagram communicates

- Same intent, different framing (baseline vs pressure)
- Scoring makes drift visible and measurable
- Failures become regression tests (so drift doesn't return)

## Future: Reference Scorer

    squeeze run --pair examples/market_certainty.yaml
    
    ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
    │  Load Pair  │ ──> │  Run A & B  │ ──> │   Score     │ ──> drift_report.json
    └─────────────┘     └─────────────┘     └─────────────┘
