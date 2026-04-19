# Triage and Root-Cause Log

This log tracks public threads where I did reproduction, root-cause isolation, scope narrowing, or technical validation follow-up. These entries are intended to show maintainer-adjacent work in public, not just merged code.

## Current entries

### 2026-04-17 - Narrowed `#1172` to the smallest merged compatibility fix
- Thread: [PR #1172](https://github.com/openai/openai-agents-js/pull/1172), [maintainer review](https://github.com/openai/openai-agents-js/pull/1172#pullrequestreview-4116689455), [follow-up comment](https://github.com/openai/openai-agents-js/pull/1172#issuecomment-4258122568)
- Type: scope narrowing, compatibility investigation, validation follow-up.
- What I did: removed the broader normalization idea, kept only the legacy `discriminatedunion` compatibility path, and reran the local verification stack before updating the PR.
- Why this is maintainer-relevant: it reduced blast radius to the smallest fix justified by the compatibility report instead of trying to merge a wider policy change.
- Outcome: PR merged on April 17, 2026.

### 2026-04-15 - Turned community issue `#1163` into a targeted compatibility fix
- Thread: [Issue #1163](https://github.com/openai/openai-agents-js/issues/1163), [PR #1171](https://github.com/openai/openai-agents-js/pull/1171)
- Type: issue-linked fix, regression scoping, compatibility follow-up.
- What I did: translated a user report about silently ignored nested audio config into a focused patch in `agents-extensions` instead of broad transport changes.
- Why this is maintainer-relevant: it converted a public bug report into a minimal upstream fix with clear scope and fast maintainer review.
- Outcome: PR approved and merged on April 15, 2026, and the issue was closed.

### 2026-04-14 - Added concrete local reproduction details for `#1166`
- Thread: [PR #1166](https://github.com/openai/openai-agents-js/pull/1166), [follow-up comment](https://github.com/openai/openai-agents-js/pull/1166#issuecomment-4245169121)
- Type: environment reproduction, contributor-tooling validation.
- What I did: documented the installed `trufflehog` version, binary path, exact updater failure mode, and why `--no-update` preserved the secret scan instead of disabling it.
- Why this is maintainer-relevant: it turned a vague local failure into a reproducible contributor-tooling bug report with enough detail to judge safety and scope.
- Outcome: PR merged on April 15, 2026.

### 2026-04-17 - Added code-level review follow-up on `#1178`
- Thread: [PR #1178](https://github.com/openai/openai-agents-js/pull/1178), [review comment 1](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3101178078), [review comment 2](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3101178272)
- Type: review-thread follow-up, usage accounting validation.
- What I did: recorded how the snapshot replacement had to update the full retry-adjusted `requestUsageEntries` slice and preserve failed-attempt placeholders in streaming usage accounting.
- Why this is maintainer-relevant: it leaves a public explanation tied to the exact code path and accounting invariant still under maintainer evaluation.
- Outcome: PR remains open pending stronger maintainer confidence.

## Entry template

### YYYY-MM-DD - Short title
- Thread:
- Type:
- What I did:
- Why this is maintainer-relevant:
- Outcome:
