# Review-Thread Validation Log

This log tracks public review comments and review-thread follow-up that improved implementation quality or validation depth.

## `#1178` - Streaming usage after `AbortSignal` cancellation

PR: [#1178](https://github.com/openai/openai-agents-js/pull/1178)

Area: `packages/agents-core`, streaming usage accounting, retries, abort handling.

### 2026-04-17 - Retry-adjusted usage accounting

- Review event: [review 1](https://github.com/openai/openai-agents-js/pull/1178#pullrequestreview-4129790723), [review 2](https://github.com/openai/openai-agents-js/pull/1178#pullrequestreview-4129790873)
- Review comments: [comment 1](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3101178078), [comment 2](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3101178272)
- Follow-up: updated snapshot replacement so retry-adjusted `requestUsageEntries` preserve failed-attempt placeholders and aggregate request totals.
- Why it matters: prevents streaming usage from under-counting request attempts after runner-managed retries.

### 2026-04-20 - Runtime probe and live validation path

- Review comment: [comment](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3111911447)
- Issue-thread follow-up: [runtime probe summary](https://github.com/openai/openai-agents-js/pull/1178#issuecomment-4281953544), [live probe instructions](https://github.com/openai/openai-agents-js/pull/1178#issuecomment-4281961306)
- Follow-up: applied retry-adjusted placeholders to streamed usage snapshots, added regression coverage for retry plus early abort, and documented how maintainers can compare `main` against the candidate branch with live OpenAI Responses streams.
- Why it matters: converts review feedback into a reproducible validation workflow rather than relying only on unit tests.

### 2026-04-21 - Streaming guard readability

- Review event: [review](https://github.com/openai/openai-agents-js/pull/1178#pullrequestreview-4148939703)
- Review comment: [comment](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3118579194)
- Follow-up: combined guard checks in `getUsageSnapshotFromStreamEvent` into a single early return.
- Why it matters: simplified the streaming event shape check without changing runtime behavior.

### 2026-04-23 - Multi-entry usage detail replacement

- Review event: [review](https://github.com/openai/openai-agents-js/pull/1178#pullrequestreview-4162886793)
- Review comment: [comment](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3131206028)
- Follow-up: identified that `UsageData` can include detail arrays and that snapshot replacement should replace the full trailing detail slice instead of only the first detail entry.
- Why it matters: keeps detailed token accounting consistent with aggregate usage when streamed snapshots include multiple detail entries.

## What Makes a Strong Entry

- It catches a runtime regression, missing test, or compatibility risk before merge.
- It narrows an implementation to the smallest justified fix.
- It turns reviewer feedback into reproducible validation.
- It links directly to public GitHub evidence.
