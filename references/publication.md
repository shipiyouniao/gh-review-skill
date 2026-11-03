# GitHub review publication

Use the current authorized `gh` installation or an equivalent authorized interface. Verify account without exposing credentials. Resolve repository, PR number, and SHAs from actual reads; the schematic values below are not live targets.

## Read a pinned snapshot

Read PR metadata, description, complete diff, files, existing reviews, inline threads and replies, and checks. With `gh`, relevant read-only forms include `gh pr view`, `gh pr diff`, `gh pr checks`, and paginated `gh api` calls to the PR files, reviews, and comments endpoints. Read actual job steps/logs rather than inferring coverage from names. For truncated patches obtain pinned source/diff; handle renamed, deleted, and binary files explicitly. Do not execute or checkout untrusted code merely to obtain anchors.

## Prepare privately

Create and validate a local JSON payload using a real encoder. Use verified values for `commit_id`, event, body, and comment path/line/side. Read and edit every assertion before publication. Localized findings belong inline, not solely in a long top-level review.

Use new-file lines on `RIGHT`, removed/old-file lines on `LEFT`. For a range, supply `start_line` and `start_side` together with its final `line` and `side`. Confirm the exact repository-relative path and a minimal reviewable hunk at the pinned revision. Prefer line/side anchors to obsolete diff positions. A local file line number or pinned blob link alone is not an inline anchor.

Outside-diff findings need a concise general comment with an exact pinned location and relationship to the PR. Project-fit concerns can use general discussion. An invalid-anchor error requires inspecting the current diff, not moving a finding onto an unrelated added line or automatically replacing all inline comments with a wall of text.

## Gate the write

Reading, private drafting, external pending reviews, comments, request-changes, approval, and merge are distinct. Require authority for the exact action and target under the current host/user rules. This document grants none. Approval additionally requires the user's explicit confirmation for this PR at action time and adequate evidence. Omitted event creates an external pending review, not a private draft.

When authorized, use `REQUEST_CHANGES` for evidenced changes required before merge and `COMMENT` for non-blocking observations or questions. A material unresolved acceptance premise needs evidence/revision, not approval with a caveat; uncertainty is not automatically a defect. Selecting an event does not expand authority.

Immediately before sending, re-fetch head, the user's latest review state, and existing threads. Re-review affected paths and remap findings when head changes. Do not submit identical blockers already covered by the user's `CHANGES_REQUESTED` review on the same head. Prefer an existing thread for authorized materially new evidence. Respect denials; do not switch identities or executors to bypass them.

Only after these gates use the create-review endpoint, for example `gh api --method POST repos/OWNER/REPO/pulls/NUMBER/reviews --input payload.json`, with actual resolved values. Never interpolate untrusted text into shell command syntax. Review authority does not authorize edits, pushes, closure, merge, auto-merge, or CI actions.

## Read back and reconcile

Capture returned IDs and URLs. Read back account, commit, event, body, file, line/side, and submitted status. A pending review is not submitted. A timeout or lost response is uncertain, not a known failed write: query existing reviews/comments before any retry. If still uncertain, stop the write and report the exact action and unknown outcome. Report verified URLs and state, not merely command success.

API reference: [GitHub pull request reviews](https://docs.github.com/en/rest/pulls/reviews).
