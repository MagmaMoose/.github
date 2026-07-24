# Contributing to Magma Moose

Thanks for being here. This is the default guide for every repository in the
[Magma Moose](https://github.com/MagmaMoose) organization. A repo that needs different rules ships
its own `CONTRIBUTING.md`, and that copy wins over this one, so if you find a `CONTRIBUTING.md` in
the repo you are working on, read that instead.

Everything below applies whether you work here or you found us through a search. There is no CLA
and no contributor agreement to sign.

## Before you write code

For a bug fix, a typo, or anything small and obvious, just open the pull request. You do not need
permission.

For a new feature, a dependency change, or anything that alters public behaviour, open an issue
first and let us agree on the shape of it. Our tools are small on purpose, and the most common
reason we turn a pull request down is that it makes one of them do a second job. Finding that out
before you build it saves you the evening.

## Setting up

Every repo has a quickstart or a development section in its README, and that is the authority on
toolchain and test commands. What is common across the org is the local hook set, which we
strongly recommend you install:

```bash
brew install calebsargeant/tap/chargate && chargate install-hooks
```

That gives you [Chargate](https://github.com/MagmaMoose/chargate)'s hooks in every repo on your
machine: a fast secret and lint scan on staged files, conventional branch name enforcement on
push, and automatic pinning of GitHub Actions to commit SHAs. Those are the same rules CI applies,
so having them locally means you find out in two seconds rather than after a round trip through
Actions. If you would rather scope it to one repo, the chargate README has a
`.pre-commit-config.yaml` snippet for that.

## Branches

Branch names follow the same conventional style as commits:

```
<type>/<short-description>
<type>/<scope>/<short-description>
```

The allowed types are `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`,
`chore` and `revert`. So `fix/action/token-scope-on-enterprise` and `docs/quickstart-permissions`
are both fine, and `calebs-branch` is not. Chargate's `conventional-branch-name` hook checks this
on push.

## Commits

We use [Conventional Commits](https://www.conventionalcommits.org/), and this one is not
cosmetic. [Diatreme](https://github.com/MagmaMoose/diatreme) reads the commit history to work out
the next semantic version, so your commit type is what decides whether the merge cuts a patch, a
minor or a major release.

```
fix(action): resolve semantic-release plugins from the co-installed tree
feat(publish): add maven, gradle and rubygems ecosystems
docs: clarify where packages publish on Enterprise
```

A few rules that follow from that:

- `fix:` produces a patch, `feat:` produces a minor, and a `BREAKING CHANGE:` footer or a `!`
  after the type produces a major. Pick the type that describes the effect on a user, not the
  effort you put in.
- **Never edit a version number or a `CHANGELOG.md` by hand.** Diatreme writes both. A manual
  edit either gets overwritten or corrupts the next computed version.
- Sign your commits if you can. We are not going to block a good pull request over it, but the
  release commits this org produces are signed, and it is nice when the history is consistent.

## Pull requests

Open the pull request against `main`. Fill in the template: what changed, why, and how you
convinced yourself it works. A pull request that changes behaviour without touching a test is the
one that gets the slowest review.

Keep it to one concern. Two unrelated fixes in one branch means neither can merge until both are
right, and it muddies the release notes that get generated from the history.

When you push, some automation happens on its own:

- **Chargate** runs the security and lint gate. It only blocks on findings your pull request
  introduces relative to the merge base, so you are never on the hook for problems that were
  already there.
- **Diatreme** verifies the build. On a repo that produces a container image it builds and pushes
  a throwaway `pr-<number>` image, which means a broken build is caught before the merge rather
  than after it. On a repo with no image to build it passes trivially.
- Both `chargate` and `diatreme` are required status checks on the default branch, so neither can
  be skipped.
- Repos that use **[Brimyr](https://github.com/MagmaMoose/brimyr)** additionally gate on the test
  coverage of the lines you changed, again ignoring what was already there.
- An automated reviewer may leave comments, and on our own branches a bot sometimes pushes the
  fixes for them. On a pull request from a fork it will only comment, never push.
- Actions have to be pinned to a commit SHA with the version in a trailing comment. If you add a
  step that uses a floating tag, the hook or the gate will tell you.

Auto-merge is available on every repo, so a pull request with it turned on merges itself the
moment reviews and required checks come back green. Head branches are deleted automatically after
a merge, which is expected rather than something going wrong, and GitHub can restore one if you
need it back.

## Releases

You do not cut releases, and neither do we by hand. Merging to the default branch triggers
Diatreme, which computes the version from the commits, writes the tag, the GitHub Release and the
changelog, and where a repo builds a container image, promotes the already-scanned image by digest
rather than rebuilding it.

The practical consequence for a contributor is simple. Get the commit message right and the
release takes care of itself.

## Reporting bugs and asking for features

Use the issue forms on the repo. The bug form asks for a version, an environment and a set of
steps, because those three are what make the difference between a bug we can reproduce this
afternoon and one that sits open for a month.

If you have found a security vulnerability, do not open an issue. Follow
[SECURITY.md](SECURITY.md) instead, which routes it privately.

If you just have a question, [SUPPORT.md](SUPPORT.md) says where to put it.

## Licensing

Contributions are accepted under the licence of the repository you are contributing to, which is
in its `LICENSE` file. Most of the org is MIT, and Dunmir is Apache-2.0. By opening a pull request
you confirm you have the right to submit the code under that licence.

The paid layers of our products live in separate private repositories, so nothing you contribute
here disappears behind a paywall.

## Conduct

Everyone taking part is covered by our [Code of Conduct](CODE_OF_CONDUCT.md). It is the
Contributor Covenant, and the short version is to be decent to people who are trying to help.
