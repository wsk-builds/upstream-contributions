# OpenAI Agents SDK Upstream Contribution Evidence

This repository is a public evidence archive for my upstream maintenance work in [openai/openai-agents-js](https://github.com/openai/openai-agents-js). It is optimized for OpenAI developer Pro / Codex for OSS review: the first screen gives the application snapshot, and the sections below link each claim to public GitHub evidence.

## One-Screen Application Summary

**Project importance.** [openai/openai-agents-js](https://github.com/openai/openai-agents-js) is OpenAI's official JavaScript/TypeScript Agents SDK for multi-agent workflows and voice agents. It is public developer infrastructure for OpenAI builders, with about `2.9k` stars and `713` forks as of April 28, 2026.

**Upstream maintenance record.** I contribute runtime, Realtime, docs, tests, and workflow maintenance to the SDK. My public record includes `9` merged upstream PRs, active runtime validation on [#1178](https://github.com/openai/openai-agents-js/pull/1178), and a supporting evidence/reporting tool in [agents-pr-tools](https://github.com/wsk-builds/agents-pr-tools).

**Release-note evidence.** The [v0.8.4 release notes](https://github.com/openai/openai-agents-js/releases/tag/v0.8.4) publicly list my merged runtime, Realtime, documentation, test, and workflow contributions: [#1170](https://github.com/openai/openai-agents-js/pull/1170), [#1171](https://github.com/openai/openai-agents-js/pull/1171), [#1172](https://github.com/openai/openai-agents-js/pull/1172), [#1158](https://github.com/openai/openai-agents-js/pull/1158), [#1160](https://github.com/openai/openai-agents-js/pull/1160), [#1165](https://github.com/openai/openai-agents-js/pull/1165), [#1162](https://github.com/openai/openai-agents-js/pull/1162), [#1169](https://github.com/openai/openai-agents-js/pull/1169), and [#1166](https://github.com/openai/openai-agents-js/pull/1166).

**Active runtime validation.** [#1178](https://github.com/openai/openai-agents-js/pull/1178) validates streaming usage after `AbortSignal` cancellation. The public thread includes review-thread follow-up, a [runtime probe summary](https://github.com/openai/openai-agents-js/pull/1178#issuecomment-4281953544), and [live probe instructions](https://github.com/openai/openai-agents-js/pull/1178#issuecomment-4281961306).

**Public outputs from Pro / API credits.** I would use 6 months of OpenAI developer Pro access for public OSS maintenance with three concrete outputs: `1` runtime regression PRs and minimized repros for streaming, retries, aborts, and usage accounting; `2` docs/example drift audits with public patches; `3` release-readiness and contribution reports through [agents-pr-tools](https://github.com/wsk-builds/agents-pr-tools) and maintainer-facing validation notes.

For a standalone reviewer page with the same snapshot, see [ONE-SCREEN-SUMMARY.md](./ONE-SCREEN-SUMMARY.md).

## High-Signal Evidence

| Signal | Public evidence | Why it matters |
| --- | --- | --- |
| Release-note inclusion | [v0.8.4 release notes](https://github.com/openai/openai-agents-js/releases/tag/v0.8.4) | Confirms the merged work shipped in an upstream OpenAI Agents SDK release. |
| Issue-to-fix flow | [Issue #1163](https://github.com/openai/openai-agents-js/issues/1163) -> merged [PR #1171](https://github.com/openai/openai-agents-js/pull/1171) | Converted a user-reported nested audio config bug into a targeted upstream compatibility fix. |
| Runtime compatibility | [#1172](https://github.com/openai/openai-agents-js/pull/1172), [#1171](https://github.com/openai/openai-agents-js/pull/1171), [#1170](https://github.com/openai/openai-agents-js/pull/1170) | Preserved tool-schema compatibility, nested audio config behavior, and SIP VAD validation. |
| Runtime validation thread | [#1178](https://github.com/openai/openai-agents-js/pull/1178), [runtime probe follow-up](https://github.com/openai/openai-agents-js/pull/1178#issuecomment-4281953544), [live probe instructions](https://github.com/openai/openai-agents-js/pull/1178#issuecomment-4281961306) | Shows review-driven validation around streaming usage, retries, aborts, and real-world probe design. |
| Documentation and workflow reliability | [#1158](https://github.com/openai/openai-agents-js/pull/1158), [#1160](https://github.com/openai/openai-agents-js/pull/1160), [#1165](https://github.com/openai/openai-agents-js/pull/1165), [#1166](https://github.com/openai/openai-agents-js/pull/1166) | Kept docs, examples, and contributor validation aligned with actual SDK usage. |

## Merged Upstream PRs

| PR | Area | Impact |
| --- | --- | --- |
| [#1172](https://github.com/openai/openai-agents-js/pull/1172) | `agents-core` runtime compatibility | Restored discriminated union tool schemas through a targeted compatibility fix. |
| [#1171](https://github.com/openai/openai-agents-js/pull/1171) | `agents-extensions` runtime compatibility | Preserved nested audio config for the bug reported in [#1163](https://github.com/openai/openai-agents-js/issues/1163). |
| [#1170](https://github.com/openai/openai-agents-js/pull/1170) | `agents-realtime` validation | Added validation for unsupported SIP VAD fields. |
| [#1169](https://github.com/openai/openai-agents-js/pull/1169) | test reliability | Stabilized the leak detection harness. |
| [#1166](https://github.com/openai/openai-agents-js/pull/1166) | contributor workflow | Preserved the pre-commit secret scan while avoiding local updater drift. |
| [#1165](https://github.com/openai/openai-agents-js/pull/1165) | docs accuracy | Fixed the Next.js example README source path. |
| [#1162](https://github.com/openai/openai-agents-js/pull/1162) | test coverage | Added AI SDK UI boundary coverage in `agents-extensions`. |
| [#1160](https://github.com/openai/openai-agents-js/pull/1160) | docs/examples | Synced AI SDK docs and examples. |
| [#1158](https://github.com/openai/openai-agents-js/pull/1158) | docs accuracy | Corrected tools example commands in the docs. |

## Active Runtime Validation Work

[#1178](https://github.com/openai/openai-agents-js/pull/1178) focuses on preserving streaming usage after `AbortSignal` cancellation. The public thread shows a validation loop around streaming usage, retries, abort handling, and live behavior probes:

| Date | Evidence | Contribution |
| --- | --- | --- |
| 2026-04-17 | [comment 1](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3101178078), [comment 2](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3101178272) | Updated retry-adjusted usage accounting so streaming usage preserves retry-attempt placeholders and aggregate totals. |
| 2026-04-20 | [runtime probe summary](https://github.com/openai/openai-agents-js/pull/1178#issuecomment-4281953544), [live probe instructions](https://github.com/openai/openai-agents-js/pull/1178#issuecomment-4281961306), [review comment](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3111911447) | Added runtime-behavior-probe analysis and ready-to-run live validation instructions. |
| 2026-04-21 | [review comment](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3118579194) | Simplified streaming guard logic without behavior changes. |
| 2026-04-23 | [review comment](https://github.com/openai/openai-agents-js/pull/1178#discussion_r3131206028) | Identified a multi-entry usage detail replacement case and committed to the corrected accounting behavior. |

Supporting logs:

- [Review-thread validation log](./logs/review-log.md)
- [Triage and root-cause log](./logs/triage-log.md)

## Supporting Tooling: `agents-pr-tools`

[agents-pr-tools](https://github.com/wsk-builds/agents-pr-tools) is a small zero-dependency CLI for generating reproducible GitHub PR reports. It supports multi-author reporting, `@me` auth resolution, state/date/area/label filters, file output, Markdown/table/JSON/CSV/release-notes formats, request retries, timeouts, and rate-limit-aware errors.

Recent tool work:

- [#4](https://github.com/wsk-builds/agents-pr-tools/pull/4): hardened GitHub API requests and CI with timeout/retry/rate-limit diagnostics.
- [#3](https://github.com/wsk-builds/agents-pr-tools/pull/3): added label filters and auth fallback.
- [#2](https://github.com/wsk-builds/agents-pr-tools/pull/2): added `@me`, file output, and CI.
- [#1](https://github.com/wsk-builds/agents-pr-tools/pull/1): added reporting modes and publish preparation.

## How Pro/Codex Would Increase Output

I would use 6 months of OpenAI developer Pro access for public OpenAI ecosystem work with concrete outputs:

| Phase | Focus | Public outputs |
| --- | --- | --- |
| Months 1-2 | Runtime regression coverage for streaming, retries, aborts, and usage accounting | Focused tests, minimized repros, and review-ready PRs in `openai/openai-agents-js`. |
| Months 3-4 | Documentation and example drift audits across Agents SDK packages | Docs patches, example fixes, and reproducible audit reports. |
| Months 5-6 | Contribution reporting and release-readiness evidence | Stronger `agents-pr-tools` reporting, release-note summaries, and maintainer-facing validation notes. |

Pro/Codex is especially useful for this work because it supports larger-context code review, faster test-case synthesis, deep issue reproduction, and clearer maintainer handoff summaries.

## Verification Links

- [Merged PR search](https://github.com/openai/openai-agents-js/pulls?q=is%3Apr+author%3Awsk-builds+is%3Amerged)
- [Runtime validation thread #1178](https://github.com/openai/openai-agents-js/pull/1178)
- [v0.8.4 release notes](https://github.com/openai/openai-agents-js/releases/tag/v0.8.4)
- [Working fork](https://github.com/wsk-builds/openai-agents-js)
- [Profile README](https://github.com/wsk-builds/wsk-builds)
