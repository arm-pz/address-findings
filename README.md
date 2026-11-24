# address-findings

An agent skill that fixes the CRITICAL and HIGH findings from a
[consistent-code-review](https://github.com/arm-pz/consistent-code-review) report on one pull request.
It only edits files the PR already changes, makes one commit per finding, and reports each finding
as **fixed**, **won't fix** (with evidence) or **escalate**. It never merges.

It is the fixer node in a review → fix → re-review → merge-gate graph.

## Install

    npx skills add arm-pz/address-findings

## Use

Ask your agent to "address the review findings on PR #N" once a review report exists.
