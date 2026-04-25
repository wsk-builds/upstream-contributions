# Triage and Root-Cause Log

This log records public threads where I performed reproduction, root-cause isolation, scope narrowing, or validation follow-up for upstream work in [openai/openai-agents-js](https://github.com/openai/openai-agents-js).

## Current Entries

### 2026-04-20 - Converted `#1178` feedback into runtime behavior probes

- Thread: [PR #1178](https://github.com/openai/openai-agents-js/pull/1178), [runtime probe summary](https://github.com/openai/openai-agents-js/pull/1178#issuecomment-4281953544), [live probe instructions](https://github.com/openai/openai-agents-js/pull/1178#issuecomment-4281961306)
- Type: runtime validation, live behavior probe design, streaming usage accounting.
- What I did: compared `main` against the candidate branch with a runtime-behavior-probe workflow, documented the branch behavior, and prepared a ready-to-run live probe for completed, early-abort, mid-abort, and late-abort streaming scenarios.
- Why this is high-signal: it turns maintainer uncertainty into a reproducible validation path with concrete pass/block/negative interpretations.
- Outcome: the PR thread now contains both local probe findings and live verification instructions maintainers can run with their own `OPENAI_API_KEY`.

### 2026-04-17 - Narrowed `#1172` to the smallest merged compatibility fix

- Thread: [PR #1172](https://github.com/openai/openai-agents-js/pull/1172), [maintainer review](https://github.com/openai/openai-agents-js/pull/1172#pullrequestreview-4116689455), [follow-up comment](https://github.com/openai/openai-agents-js/pull/1172#issuecomment-4258122568)
- Type: scope narrowing, compatibility investigation, validation follow-up.
- What I did: removed the broader normalization idea, kept only the legacy `discriminatedunion` compatibility path, and reran the local verification stack before updating the PR.
- Why this is high-signal: it reduced blast radius to the smallest fix justified by the compatibility report.
- Outcome: PR merged on April 17, 2026.

### 2026-04-15 - Turned community issue `#1163` into a targeted compatibility fix

- Thread: [Issue #1163](https://github.com/openai/openai-agents-js/issues/1163), [PR #1171](https://github.com/openai/openai-agents-js/pull/1171)
- Type: issue-linked fix, regression scoping, compatibility follow-up.
- What I did: translated a user report about silently ignored nested audio config into a focused patch in `agents-extensions`.
- Why this is high-signal: it converted a public bug report into a minimal upstream fix with clear scope and fast maintainer review.
- Outcome: PR approved and merged on April 15, 2026, and the issue was closed.

### 2026-04-14 - Added concrete local reproduction details for `#1166`

- Thread: [PR #1166](https://github.com/openai/openai-agents-js/pull/1166), [follow-up comment](https://github.com/openai/openai-agents-js/pull/1166#issuecomment-4245169121)
- Type: environment reproduction, contributor-tooling validation.
- What I did: documented the installed `trufflehog` version, binary path, exact updater failure mode, and why `--no-update` preserved the secret scan instead of disabling it.
- Why this is high-signal: it turned a vague local failure into a reproducible contributor-tooling fix with enough detail to judge safety and scope.
- Outcome: PR merged on April 15, 2026.

### 2026-04-17 to 2026-04-23 - Code-level follow-up on `#1178`

- Thread: [PR #1178](https://github.com/openai/openai-agents-js/pull/1178), [review log](./review-log.md)
- Type: review-thread follow-up, usage accounting validation.
- What I did: iterated on retry-adjusted request entries, streamed usage snapshots, guard readability, and multi-entry detail replacement.
- Why this is high-signal: it leaves public, code-linked reasoning for correctness invariants that are difficult to validate by inspection alone.
- Outcome: active runtime validation thread remains public and reviewable.

## Entry Template

### YYYY-MM-DD - Short title

- Thread:
- Type:
- What I did:
- Why this is high-signal:
- Outcome:
