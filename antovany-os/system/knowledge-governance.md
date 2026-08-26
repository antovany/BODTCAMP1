# Knowledge Governance

## Objective

Keep Antovany OS useful, auditable, current, and safe across human and AI workflows.

## Evidence status

Each consequential claim should use one of these statuses:

- `VERIFIED` — directly supported by a reliable canonical source.
- `SUPPORTED` — supported by credible evidence but not fully primary-source verified.
- `HYPOTHESIS` — plausible inference that still requires testing.
- `NEEDS_VALIDATION` — important but insufficiently supported.
- `TIME_SENSITIVE` — may become stale and must include an `as_of` date.

## Privacy classes

- `PUBLIC` — suitable for websites, public GitHub, portfolios, and external AI contexts.
- `INTERNAL` — useful for personal operating systems but not intended for publication.
- `CONFIDENTIAL` — commercially, legally, professionally, or personally sensitive.
- `RESTRICTED` — secrets, credentials, identity documents, highly sensitive evidence, or information whose exposure can create material harm.

Only `PUBLIC` information belongs in this public GitHub layer.

## Redaction rule

If an internal insight is strategically useful but not public-safe, create a derivative containing only the minimum necessary abstraction. Preserve a pointer to the private canonical source instead of reproducing sensitive details.

## Temporal hygiene

For information that changes with time:

1. store `as_of`;
2. set `review_after` where appropriate;
3. distinguish historical fact from current state;
4. do not silently overwrite an important historical decision or assumption;
5. keep change history through Git commits or source-system revision history.

## Contradiction handling

When sources conflict:

1. retain both claims;
2. record source and date;
3. rank source authority;
4. state the unresolved contradiction;
5. avoid collapsing uncertainty into a false single truth;
6. resolve only when stronger evidence emerges.

## AI ingestion rule

AI assistants should not treat all KBMS entries as equally authoritative. Prefer, in order:

1. canonical primary evidence;
2. verified structured knowledge;
3. supported synthesis;
4. hypotheses;
5. speculative or stale notes.

## Quality test before promoting knowledge

A knowledge object should answer:

- What is the claim?
- What supports it?
- When was it true?
- How confident are we?
- What could falsify it?
- Why does it matter?
- Is it safe to expose in this destination?

**As of:** 2026-08-26
