# Squeeze — Methodology v1.0

**Author:** Tracy Pertner

Squeeze is a method for drilling down, spotting loopholes, pressure-testing claims, and turning "vibes" into tests, checklists, and measurable outputs.

This repo uses Squeeze specifically to detect **drift** in LLM behavior (trust drift, compliance drift, and relational/tone drift) using **pressure-tested prompt pairs** and simple scoring rubrics.

## When to use Squeeze

Use this method when you want:

- actionable + measurable outcomes (not just ideas)
- edge cases and failure modes surfaced early
- messy reality turned into a system
- evals, QA plans, experiment design, or "ship the v0"
- drift detection: "the model felt different" → a repeatable test

## Inputs (use what you have)

- Goal
- Scope (in / out)
- Constraints (time, tools, audience, risk tolerance)
- Current artifacts (files, logs, drafts, links)
- Success definition (what "done" means)

If inputs are missing, Squeeze will propose defaults and keep moving.

## Rules

1) No fog: ask 1–2 clarifiers or state assumptions explicitly.
2) Convert everything into a deliverable: tests, rubric, checklist, template, or commands.
3) Loophole hunting is allowed (and productive): find failure modes and prompt-pressure drift.
4) Truth over pleasing: no fake citations, no pretending.
5) Small bites, fast wins: ship v0 today > perfect v10 later.
6) Evidence > vibes: use minimal repros and measurable acceptance criteria.

## Drift method (how we test "it felt different")

Squeeze drift tests use **A/B prompt pairs**:

- **A (baseline):** neutral prompt
- **B (pressure):** same intent, but with one stressor (urgency, authority, coercion, flattery, "no hedging," etc.)

We score changes using simple checks such as:

- **Calibration / truthfulness:** no invented facts, no fake certainty under pressure
- **Policy / boundaries:** doesn't comply more when bullied
- **Tone / relational stability:** warm without becoming clingy, exclusive, or escalatory
- **Helpfulness:** still offers safe alternatives and next steps

Output should be a pasteable artifact (YAML case, checklist, or report) so drift becomes a regression test.

## Output formats

- Eval pack (YAML cases + scoring rules + thresholds)
- QA plan (test matrix + severity + repro steps)
- Experiment plan (hypotheses + variables + pass/fail)
- Repo scaffold (file tree + commands + README language)

## Success metrics

Squeeze is succeeding if:

- we produce a usable artifact each session
- you can run/paste/ship it
- ambiguity decreases
- failures become regression tests
- progress is trackable (pass rate, flaky rate, severity-5 count)

## Default deliverable

If you invoke Squeeze without specifics, it returns:

1) next 3 actions (commands/steps)
2) a reusable template
3) one key failure mode to watch for
