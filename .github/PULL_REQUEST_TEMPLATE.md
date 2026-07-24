<!--
Thanks for the pull request. The sections below are what reviewers actually read, so
please fill them in rather than deleting them. If a section genuinely does not apply,
write "n/a" and why.

Reminder: the commit message decides the release. Conventional Commits are enforced,
and Diatreme reads them to compute the next semantic version. Do not edit version
numbers or CHANGELOG.md by hand.
-->

## What this changes

<!-- One or two sentences in plain language. What is different after this merges? -->

## Why

<!-- The problem this solves. Link the issue it closes, for example "Closes #123". -->

## How it was tested

<!--
How did you convince yourself this works? Tests you added, commands you ran, the
output you saw. "CI is green" on its own does not count if the change is behavioural.
-->

## Breaking changes

<!--
Anything that makes an existing user's setup behave differently: renamed or removed
inputs, changed defaults, new required permissions, a different output shape.

If there are any, say so here AND put a `BREAKING CHANGE:` footer in the commit, so
the release comes out as a major.
-->

## Checklist

- [ ] The branch name follows `<type>/<description>` and the commits follow Conventional Commits.
- [ ] Docs and the README are updated if behaviour or configuration changed.
- [ ] Tests cover the change, or there is a note above explaining why they cannot.
- [ ] No version numbers or changelog entries were edited by hand.
- [ ] Any new GitHub Actions steps are pinned to a commit SHA with the version in a trailing comment.
- [ ] No secrets, tokens, customer data or internal hostnames are in the diff.
