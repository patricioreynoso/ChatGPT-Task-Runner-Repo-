# ChatGPT Task Runner

Pilot repository for testing scoped task handoffs from ChatGPT through GitHub to a Cursor automation.

## Prepared workflow

1. Describe a bounded task in a GitHub issue, including context, allowed scope, and acceptance checks.
2. Configure the Cursor automation for GitHub issue comments on this repository. The current interface shows this event; the previously attempted label trigger watches pull requests.
3. After the configuration is saved, the repository owner (`patricioreynoso`) posts an issue comment whose trimmed body is exactly `/cursor-task` to request execution. The automation instructions must reject other authors and comments.
4. Cursor works on a separate branch and opens a draft pull request linked to the issue. If a PR already addresses the issue, it stops instead of duplicating the work.
5. Review the changed files and the checks actually run before accepting the result.

## Status

The issue-comment route is prepared as a compatibility option; its saved Cursor configuration and first execution remain unverified. ChatGPT has successfully posted and read back a non-command setup comment on the test issue.

This repository is a test harness. These setup steps do not verify the Cursor execution loop or the return path to the Project Brain. The `cursor-task` label is not required for the prepared comment-trigger route.

Task execution must not merge or deploy changes. The first test is documentation-only.
