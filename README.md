# address-findings

An agent skill that fixes the CRITICAL and HIGH findings from a
[consistent-code-review](https://github.com/arm-pz/consistent-code-review) report on one pull request.
It only edits files the PR already changes, makes one commit per finding, and reports each finding
as **fixed**, **won't fix** (with evidence) or **escalate**. It never merges, never force-pushes,
and escalates when it can't write to the PR's head repository.

It is the fixer node in a review → fix → re-review → merge-gate graph.

## Install

- Upload `address-findings.zip` in your skills settings, or
- Copy this folder into `~/.claude/skills/address-findings/` (or the project's `.claude/skills/`), or
- `npx skills add arm-pz/address-findings`

Check it worked: `address-findings` appears in the agent's skill list.

## Try it

- "Address the review findings on PR #77"
- "Fix the CRITICAL and HIGH issues the reviewer flagged on this PR"
- "Resolve the blocking review comments on #40"

It needs a `review-report.json` for the PR; without one, run consistent-code-review first.

## Boundaries

- Handles: CRITICAL and HIGH findings on one PR, inside that PR's changed files.
- Does not handle: writing a review (consistent-code-review), new features, rebasing for conflicts, or merging (`merge_gate.py` decides).

## Test results

- Version 0.2.0: 0 pass, 0 fail, 11 reviewed-only, 0 not run. Read-through of the description only; no live-session run.

## Version

See CHANGELOG.md.
