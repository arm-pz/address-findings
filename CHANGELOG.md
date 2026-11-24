# Changelog

## 0.2.0 (2026-11-24)
- Synced with the PR graph variant: skip labels (`hands-off`, `needs-owner`; `hold` allows fixes), report `repository` check, `{owner}/{repo}` commands, target-repo baseline, push to the head repository (escalate if unwritable), `repository` in fix-report.
- Kept the broader trigger wording from 0.1.0 tuning. Standalone is now the source of truth; pr-graph vendors it.
- Tests: description unchanged from 0.1.0 (11 reviewed-only, none run live).

## 0.1.0 (2026-11-24)
- Initial release: fixes CRITICAL and HIGH findings from a consistent-code-review report on one PR, inside the PR's own files, one commit per finding.
- Tests: 0 pass, 0 fail, 11 reviewed-only (description read-through, no live session), 0 not run.
