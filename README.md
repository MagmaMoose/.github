# .github

This is the Magma Moose organization's meta repository. It holds two things: the profile page you
see at [github.com/MagmaMoose](https://github.com/MagmaMoose), and the default community health
files that every other repo in the org inherits.

Nothing here ships to users. If you are looking for the tools, start at
[magmamoose.com](https://magmamoose.com) or the [profile page](https://github.com/MagmaMoose).

## What is in here

| Path | What it does |
| --- | --- |
| [`profile/README.md`](profile/README.md) | Rendered as the organization profile page. This is the front door, so keep it current. |
| [`profile/assets/`](profile/assets) | The profile banner. Generated, not drawn: it is `githubBanner()` in the website repo's `brand/generate/gen.js`, copied here because this repo is public and that one is not. To change it, change the generator, run the brand build, and recopy. |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Contributor Covenant 2.1, with our enforcement contact filled in. |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | How to work in any Magma Moose repo: branches, commits, reviews, releases. |
| [`SECURITY.md`](SECURITY.md) | How to report a vulnerability privately, and what happens after you do. |
| [`SUPPORT.md`](SUPPORT.md) | Where to ask questions, and what response to expect. |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | The default pull request body. |
| [`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE) | The default bug report and feature request forms, plus the contact links shown on the "New issue" screen. |

## How the inheritance works

GitHub falls back to this repository whenever a repo in the org does not carry its own copy of a
community health file. A repo that defines its own `SECURITY.md`, `CONTRIBUTING.md` or issue
template always wins, and the fallback applies per file rather than all or nothing.

Two consequences are worth remembering:

1. **Editing a file here changes the answer for every repo that has not overridden it.** That is
   the point, but it does mean a careless edit is an org-wide one.
2. **Forks and source archives do not inherit anything.** If a repo needs its policy to travel
   with the code, give that repo its own copy.

## What is deliberately not here

- **No `FUNDING.yml`.** Magma Moose is a studio funded by engineering work rather than a
  donation-funded project, so a sponsor button would be misleading.
- **No `workflow-templates/`.** Starter workflows would duplicate the real thing and then drift
  from it. Shared CI, security and release workflows are reconciled onto every repo by
  [Caldrith](https://github.com/MagmaMoose/caldrith) from `.github/settings.yml` in the private
  `admin` repo, which stays the single source of truth for them.
- **No CI of its own.** Caldrith deliberately excludes this repo and `admin` from management, and
  there is nothing here to build, test or release.

## Changing something

Open a pull request rather than pushing to `main`, the same as anywhere else in the org. Changes
to `profile/README.md` are public the moment they merge, so read them once more before you press
the button.
