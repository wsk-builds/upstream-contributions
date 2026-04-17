# Upstream Contributions for `openai/openai-agents-js`

This repository is a public evidence index for my upstream maintenance work in [openai/openai-agents-js](https://github.com/openai/openai-agents-js), with direct links back to the source pull requests, comments, and working branches.

## Snapshot
- Upstream project: [openai/openai-agents-js](https://github.com/openai/openai-agents-js) with `2,685` stars and `681` forks as of April 16, 2026.
- Public activity window tracked here: April 11, 2026 to present.
- Public contribution record: [7 merged PRs](https://github.com/openai/openai-agents-js/pulls?q=is%3Apr+author%3Awsk-builds+is%3Amerged) and [6 open PRs](https://github.com/openai/openai-agents-js/pulls?q=is%3Apr+author%3Awsk-builds+is%3Aopen).
- Current focus modules: [`agents-extensions`](https://github.com/openai/openai-agents-js/pulls?q=is%3Apr+author%3Awsk-builds+label%3Apackage%3Aagents-extensions), [`agents-realtime`](https://github.com/openai/openai-agents-js/pulls?q=is%3Apr+author%3Awsk-builds+label%3Apackage%3Aagents-realtime), [`agents-core`](https://github.com/openai/openai-agents-js/pulls?q=is%3Apr+author%3Awsk-builds+label%3Apackage%3Aagents-core), and maintenance workflow fixes.
- Working fork: [wsk-builds/openai-agents-js](https://github.com/wsk-builds/openai-agents-js).

## Evidence links
- [Merged PR search](https://github.com/openai/openai-agents-js/pulls?q=is%3Apr+author%3Awsk-builds+is%3Amerged)
- [Open PR search](https://github.com/openai/openai-agents-js/pulls?q=is%3Apr+author%3Awsk-builds+is%3Aopen)
- [Issue and PR comment search](https://github.com/openai/openai-agents-js/issues?q=commenter%3Awsk-builds)
- [PR review search](https://github.com/openai/openai-agents-js/pulls?q=is%3Apr+reviewed-by%3Awsk-builds)
- [Working fork branches](https://github.com/wsk-builds/openai-agents-js/branches)

## Focus modules

### `agents-extensions`
- Merged [#1171](https://github.com/openai/openai-agents-js/pull/1171): preserve nested audio config.
- Merged [#1162](https://github.com/openai/openai-agents-js/pull/1162): add AI SDK UI boundary coverage.
- Merged [#1160](https://github.com/openai/openai-agents-js/pull/1160): sync AI SDK docs and examples.

### `agents-realtime`
- Merged [#1170](https://github.com/openai/openai-agents-js/pull/1170): fail fast on unsupported SIP VAD fields.
- Open [#1175](https://github.com/openai/openai-agents-js/pull/1175): replay assistant audio history from transcripts.

### `agents-core`
- Open [#1172](https://github.com/openai/openai-agents-js/pull/1172): restore discriminated union tool schemas.
- Open [#1169](https://github.com/openai/openai-agents-js/pull/1169): stabilize the leak detection harness.

### Cross-cutting maintenance
- Merged [#1166](https://github.com/openai/openai-agents-js/pull/1166): disable trufflehog auto-update in pre-commit.
- Merged [#1165](https://github.com/openai/openai-agents-js/pull/1165): fix the Next.js example README source path.
- Merged [#1158](https://github.com/openai/openai-agents-js/pull/1158): correct tools example commands in the docs.
- Open [#1180](https://github.com/openai/openai-agents-js/pull/1180): normalize compacted multimodal session items.
- Open [#1178](https://github.com/openai/openai-agents-js/pull/1178): preserve streaming usage after `AbortSignal` cancellation.
- Open [#1179](https://github.com/openai/openai-agents-js/pull/1179): implement the forcing-tool-use calculator example.

## Current open upstream PRs
- [#1180](https://github.com/openai/openai-agents-js/pull/1180): `fix(openai)` normalize compacted multimodal session items.
- [#1179](https://github.com/openai/openai-agents-js/pull/1179): `fix(examples)` implement forcing-tool-use calculator.
- [#1178](https://github.com/openai/openai-agents-js/pull/1178): `fix` preserve streaming usage after `AbortSignal` cancellation.
- [#1175](https://github.com/openai/openai-agents-js/pull/1175): `fix(realtime)` replay assistant audio history from transcripts.
- [#1172](https://github.com/openai/openai-agents-js/pull/1172): `fix(agents-core)` restore discriminated union tool schemas.
- [#1169](https://github.com/openai/openai-agents-js/pull/1169): `test(agents-core)` stabilize leak detection harness.

## Verified merged upstream PRs
- [#1171](https://github.com/openai/openai-agents-js/pull/1171): `fix(agents-extensions)` preserve nested audio config.
- [#1170](https://github.com/openai/openai-agents-js/pull/1170): `fix(agents-realtime)` fail fast on unsupported SIP VAD fields.
- [#1166](https://github.com/openai/openai-agents-js/pull/1166): `fix(husky)` disable trufflehog auto-update in pre-commit.
- [#1165](https://github.com/openai/openai-agents-js/pull/1165): `docs(nextjs)` fix README source path.
- [#1162](https://github.com/openai/openai-agents-js/pull/1162): `test(agents-extensions)` add AI SDK UI boundary coverage.
- [#1160](https://github.com/openai/openai-agents-js/pull/1160): `docs(agents-extensions)` sync AI SDK docs and examples.
- [#1158](https://github.com/openai/openai-agents-js/pull/1158): `docs` fix tools example commands.
