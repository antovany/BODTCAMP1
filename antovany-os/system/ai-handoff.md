# AI Handoff Protocol

## Purpose

Enable different AI assistants, agents, or future models to continue Antovany OS work without losing context, confusing hypotheses with facts, or exposing private information.

## Minimum handoff packet

Every substantial handoff should contain:

1. **Objective** — what outcome is being pursued.
2. **Current state** — what has already been decided or completed.
3. **Canonical sources** — where the authoritative evidence lives.
4. **Known facts** — only evidence-backed statements.
5. **Open hypotheses** — assumptions still requiring validation.
6. **Constraints** — legal, commercial, privacy, timing, budget, or format constraints.
7. **Decision log** — important decisions and rationale.
8. **Next actions** — prioritized actions with owners or expected outputs.
9. **Staleness markers** — `as_of` date and what needs refreshing.
10. **Privacy class** — PUBLIC / INTERNAL / CONFIDENTIAL / RESTRICTED.

## AI behavior contract

An AI consuming Antovany OS context should:

- distinguish evidence from interpretation;
- preserve uncertainty instead of inventing certainty;
- use current sources for time-sensitive claims;
- prefer canonical sources over summaries;
- identify contradictions explicitly;
- avoid copying confidential material into public destinations;
- update the knowledge object when a decision materially changes;
- optimize for decision usefulness, not merely information volume.

## Suggested handoff format

```yaml
objective: ""
as_of: YYYY-MM-DD
privacy: PUBLIC|INTERNAL|CONFIDENTIAL|RESTRICTED
status: active|paused|completed|archived
canonical_sources: []
known_facts: []
hypotheses: []
constraints: []
decisions:
  - decision: ""
    rationale: ""
    date: YYYY-MM-DD
next_actions: []
review_triggers: []
```

## Context compression principle

Do not transfer the entire archive by default. Transfer the smallest context set that preserves:

- strategic intent,
- non-obvious constraints,
- key evidence,
- unresolved uncertainty,
- prior decisions that should not be re-litigated without new evidence.

This keeps AI collaboration efficient while maintaining institutional memory.

**As of:** 2026-08-26
