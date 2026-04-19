# Upstream Contributions for `openai/openai-agents-js`

This repository is a public evidence page for my upstream maintenance work in [openai/openai-agents-js](https://github.com/openai/openai-agents-js). It is organized around verifiable maintainer signals: merged code, issue-linked follow-up, review-thread participation, and public maintainer feedback.

For a reviewer-oriented application version, see [ONE-SCREEN-SUMMARY.md](./ONE-SCREEN-SUMMARY.md).

## Snapshot
- Upstream project: [openai/openai-agents-js](https://github.com/openai/openai-agents-js) with `2,741` stars and `688` forks as of April 19, 2026.
- Public authored upstream PRs in `openai/openai-agents-js`: `15` total, `9` merged, `1` open.
- Public discussion footprint in the upstream repo: `7` issue/PR comment threads plus `2` submitted review events and `2` review comments visible in the public event feed.
- Working fork: [wsk-builds/openai-agents-js](https://github.com/wsk-builds/openai-agents-js).
- Profile README: [wsk-builds/wsk-builds](https://github.com/wsk-builds/wsk-builds).

## Evidence Map
- [One-Screen Summary](./ONE-SCREEN-SUMMARY.md): application-style overview optimized for a fast reviewer pass.
- [Merged PRs](#merged-prs): runtime fixes, test stabilization, docs corrections, and maintainer-workflow patches accepted upstream.
- [Issue Triage and Technical Follow-up](#issue-triage-and-technical-follow-up): issue-linked fixes, reproduction details, scope narrowing, and public validation notes.
- [PR Reviews and Review-thread Follow-up](#pr-reviews-and-review-thread-follow-up): current public review participation and direct links to the review threads.
- [Maintainer Acknowledgements](#maintainer-acknowledgements): approvals, merges, and maintainer feedback that shaped scope or clarified ownership boundaries.
- Supporting logs: [triage log](./logs/triage-log.md), [review log](./logs/review-log.md), [maintainer interactions](./logs/maintainer-interactions.md), and the [logging guide](./logs/README.md).

## Merged PRs

### Runtime and compatibility
- [#1172](https://github.com/openai/openai-agents-js/pull/1172): `fix(agents-core)` restore discriminated union tool schemas. Narrowed after maintainer review and merged by [`@seratch`](https://github.com/seratch) on April 17, 2026.
- [#1171](https://github.com/openai/openai-agents-js/pull/1171): `fix(agents-extensions)` preserve nested audio config for the bug reported in [issue #1163](https://github.com/openai/openai-agents-js/issues/1163). Approved and merged by [`@seratch`](https://github.com/seratch) on April 15, 2026.
- [#1170](https://github.com/openai/openai-agents-js/pull/1170): `fix(agents-realtime)` fail fast on unsupported SIP VAD fields. Approved and merged by [`@seratch`](https://github.com/seratch) on April 15, 2026.

### Test stabilization
- [#1169](https://github.com/openai/openai-agents-js/pull/1169): `test` stabilize the leak detection harness. Public maintainer comment, approval, and merge by [`@seratch`](https://github.com/seratch) on April 17, 2026.
- [#1162](https://github.com/openai/openai-agents-js/pull/1162): `test(agents-extensions)` add AI SDK UI boundary coverage. Approved and merged by [`@seratch`](https://github.com/seratch) on April 15, 2026.

### Docs and maintenance workflow
- [#1166](https://github.com/openai/openai-agents-js/pull/1166): `fix(husky)` disable trufflehog auto-update in pre-commit. Merged after a public environment-reproduction comment.
- [#1165](https://github.com/openai/openai-agents-js/pull/1165): `docs(nextjs)` fix the example README source path.
- [#1160](https://github.com/openai/openai-agents-js/pull/1160): `docs(agents-extensions)` sync AI SDK docs and examples.
- [#1158](https://github.com/openai/openai-agents-js/pull/1158): `docs` correct tools example commands in the docs.

## Issue Triage and Technical Follow-up
- [Issue #1163](https://github.com/openai/openai-agents-js/issues/1163) to [PR #1171](https://github.com/openai/openai-agents-js/pull/1171): turned a community bug report about silently ignored nested audio config into a targeted compatibility fix that was approved and merged upstream.
- [PR #1166 follow-up comment](https://github.com/openai/openai-agents-js/pull/1166#issuecomment-4245169121): documented the local `trufflehog` version, binary path, updater failure mode, and why `--no-update` preserved the secret scan instead of disabling it.
- [PR #1172 maintainer review](https://github.com/openai/openai-agents-js/pull/1172#pullrequestreview-4116689455) and [follow-up comment](https://github.com/openai/openai-agents-js/pull/1172#issuecomment-4258122568): reduced a broader compatibility idea to the smallest demonstrated fix, reran validation, and got the narrowed change merged.
- [PR #1178 review-thread follow-up](https://github.com/openai/openai-agents-js/pull/1178): posted targeted code-level responses in review threads for retry-adjusted usage accounting while the PR remains under maintainer evaluation.

## PR Reviews and Review-thread Follow-up
- Public review participation currently visible:
  - [Review thread 1 on #1178](https://github.com/openai/openai-agents-js/pull/1178#pullrequestreview-4129790723)
  - [Review thread 2 on #1178](https://github.com/openai/openai-agents-js/pull/1178#pullrequestreview-4129790873)
  - [Review comment 1 on #1178](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3101178078)
  - [Review comment 2 on #1178](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3101178272)
- Those review comments document why the usage snapshot replacement has to update the full retry-adjusted `requestUsageEntries` slice and preserve failed-attempt placeholders when streaming usage is recomputed.
- Current boundary: the public review record here is still concentrated on follow-up inside my own upstream PR threads. Outbound review on other contributors' PRs is the next area I am making public and trackable.

## Maintainer Acknowledgements
- [`@seratch`](https://github.com/seratch) merged all `9` currently merged `openai/openai-agents-js` PRs listed on this page.
- Explicit approval reviews from [`@seratch`](https://github.com/seratch) are publicly visible on [#1158](https://github.com/openai/openai-agents-js/pull/1158), [#1162](https://github.com/openai/openai-agents-js/pull/1162), [#1165](https://github.com/openai/openai-agents-js/pull/1165), [#1166](https://github.com/openai/openai-agents-js/pull/1166), [#1169](https://github.com/openai/openai-agents-js/pull/1169), [#1170](https://github.com/openai/openai-agents-js/pull/1170), [#1171](https://github.com/openai/openai-agents-js/pull/1171), and [#1172](https://github.com/openai/openai-agents-js/pull/1172).
- Public maintainer direction that materially changed scope or clarified boundaries:
  - [#1172](https://github.com/openai/openai-agents-js/pull/1172): requested a narrower fix before later approving the merged version.
  - [#1164](https://github.com/openai/openai-agents-js/pull/1164): clarified design intent and closed a docs PR that did not match maintainer intent.
  - [#1171 comment](https://github.com/openai/openai-agents-js/pull/1171#issuecomment-4268944640): clarified that labels and project operations stay with maintainers even when contributor technical follow-up is helpful.
  - [#1178 comment](https://github.com/openai/openai-agents-js/pull/1178#issuecomment-4272253022): requested stronger validation before merge.

## Current Open Upstream Work
- [#1178](https://github.com/openai/openai-agents-js/pull/1178): `fix` preserve streaming usage after `AbortSignal` cancellation.

## Supporting Logs
- [logs/triage-log.md](./logs/triage-log.md)
- [logs/review-log.md](./logs/review-log.md)
- [logs/maintainer-interactions.md](./logs/maintainer-interactions.md)
- [logs/README.md](./logs/README.md)
