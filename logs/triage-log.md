# Triage and Root-Cause Log

This log tracks public threads where I did reproduction, root-cause isolation, scope narrowing, or technical validation follow-up. These entries are intended to show maintainer-adjacent work in public, not just merged code.

## Current entries

### 2026-04-16 — Narrowed `#1172` to the smallest demonstrated fix
- Thread: [PR #1172](https://github.com/openai/openai-agents-js/pull/1172), [maintainer review](https://github.com/openai/openai-agents-js/pull/1172#pullrequestreview-4116689455), [follow-up comment](https://github.com/openai/openai-agents-js/pull/1172#issuecomment-4258122568)
- Type: scope narrowing, compatibility investigation, validation follow-up.
- What I did: removed the broader `oneOf` to `anyOf` normalization approach, kept only the legacy `discriminatedunion` compat path, and reran the full local verification stack.
- Why this is maintainer-relevant: it reduces blast radius to the smallest fix justified by a live compatibility gap instead of trying to merge a broad policy change.
- Outcome: PR is still open with a narrower claim and smaller diff.

### 2026-04-14 — Added concrete local reproduction details for `#1166`
- Thread: [PR #1166](https://github.com/openai/openai-agents-js/pull/1166), [follow-up comment](https://github.com/openai/openai-agents-js/pull/1166#issuecomment-4245169121)
- Type: environment repro, contributor-tooling validation.
- What I did: documented the installed `trufflehog` version, binary path, exact updater failure mode, and why `--no-update` preserves the secret scan instead of disabling it.
- Why this is maintainer-relevant: it turns a vague local failure into a reproducible contributor-tooling bug report with enough detail to judge safety and scope.
- Outcome: PR merged on 2026-04-15.

## Entry template

### YYYY-MM-DD — Short title
- Thread:
- Type:
- What I did:
- Why this is maintainer-relevant:
- Outcome:
