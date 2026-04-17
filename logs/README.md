# Maintainer Signal Logging Guide

This directory tracks public evidence that looks more like maintenance work than a plain list of merged PRs. The goal is to make it easy for an outside reviewer to verify technical follow-up, public reviews, and interactions with upstream maintainers.

## What belongs here
- `triage-log.md`: issue reproduction, root-cause isolation, scope narrowing, validation notes, and public technical follow-up.
- `review-log.md`: public PR reviews or review comments left on other contributors' pull requests.
- `maintainer-interactions.md`: public maintainer feedback that changed the shape of the work, closed a thread, requested a narrower fix, or clarified design intent.

## Entry rules
- Only record public GitHub evidence. If it is not visible on GitHub, it does not belong in these logs.
- Link to the exact PR, issue, review, or comment, not just the repository.
- State the maintainer value in one sentence. A good entry explains why the activity reduced review load, narrowed scope, improved reproducibility, or clarified intent.
- Prefer a small number of high-signal entries over a long list of weak ones.
- When a thread changes direction because of maintainer feedback, update both `triage-log.md` and `maintainer-interactions.md` if both perspectives matter.

## Fast update checklist
1. Add or update the relevant log entry.
2. If merged or open PR counts changed, refresh the top-level `README.md` snapshot.
3. If focus modules changed, refresh the `README.md` focus section.
4. If there was a maintainer review, closure, or scope correction, update `maintainer-interactions.md`.
5. If the work was a review on someone else's PR, update `review-log.md`.
