# ChatGPT Task Runner

Pilot repository for testing scoped task handoffs from ChatGPT through GitHub to a Cursor automation.

## Intended workflow

1. Describe a bounded task in a GitHub issue, including context, allowed scope, and acceptance checks.
2. Add the `cursor-task` label after the Cursor issue-label trigger is configured.
3. Cursor works on a separate branch and opens a draft pull request linked to the issue.
4. Review the changed files and the checks actually run before accepting the result.

## Status

This repository is a test harness. Repository initialization does not verify that the Cursor automation or the return path to ChatGPT is working.

Task execution must not merge or deploy changes. The first test is documentation-only.
