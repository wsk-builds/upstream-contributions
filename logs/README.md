# Evidence Logging Guide

This directory tracks public evidence that looks more like maintenance work than a plain list of merged PRs. The goal is to make it easy for an outside reviewer to verify technical follow-up, review-thread validation, and reproducible upstream maintenance work.

## What belongs here
- `triage-log.md`: issue reproduction, root-cause isolation, scope narrowing, validation notes, and public technical follow-up.
- `review-log.md`: public review comments and review-thread validation that can be verified from GitHub.

## Entry rules
- Only record public GitHub evidence. If it is not visible on GitHub, it does not belong in these logs.
- Link to the exact PR, issue, review, or comment, not just the repository.
- State the maintainer value in one sentence. A good entry explains why the activity reduced review load, improved reproducibility, or clarified runtime behavior.
- Prefer a small number of high-signal entries over a long list of weak ones.

## Fast update checklist
1. Add or update the relevant log entry.
2. If merged or open PR counts changed, refresh the top-level `README.md` snapshot.
3. If focus modules changed, refresh the `README.md` focus section.
4. If the work created a public review event or review comment, update `review-log.md`.
