# Review Log

This log tracks public PR reviews, review comments, and review-thread follow-up that can be verified on GitHub.

## Current public entries

### 2026-04-17 - Review-thread follow-up on `#1178`
- PR: [#1178](https://github.com/openai/openai-agents-js/pull/1178)
- Reviews: [review 1](https://github.com/openai/openai-agents-js/pull/1178#pullrequestreview-4129790723), [review 2](https://github.com/openai/openai-agents-js/pull/1178#pullrequestreview-4129790873)
- Review comments: [comment 1](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3101178078), [comment 2](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3101178272)
- Area: `packages/agents-core/src/usage.ts`
- Main feedback: documented why `replaceCurrentRequestSnapshot()` must update request totals and replace the full retry-adjusted `requestUsageEntries` contribution so streaming usage does not under-count requests after retries.
- Why this is maintainer-relevant: it leaves a public code-review trail tied to the exact accounting invariant under discussion instead of burying the rationale in commits alone.
- Outcome: PR remains open for more maintainer validation.

## Current boundary
- No public outbound reviews on other contributors' pull requests are recorded here yet.
- New outbound reviews should be added here as soon as they exist.

## What a strong entry looks like
- Catches a regression, missing test, or compatibility risk before merge.
- Narrows an over-broad change to the smallest justified fix.
- Flags docs drift, release-note impact, or user-facing behavior changes.
- Links directly to the review thread so the feedback can be verified quickly.

## Entry template

### YYYY-MM-DD - PR #NNNN short title
- PR:
- Review link:
- Area:
- Main feedback:
- Why this is maintainer-relevant:
- Outcome:
