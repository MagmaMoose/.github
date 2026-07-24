# Magma Moose

**Small, sharp tools for teams that ship.**

Magma Moose builds focused, open-core tools for the unglamorous parts of shipping software and
running infrastructure. The release spine. The security gate. The maintenance you have to be able
to trust. Each tool does a single job properly, the core is free and open, and there is a paid
layer only where the work is genuinely worth paying for.

All of it exists because we needed it ourselves first, and then kept it open because other people
have the same problems.

## What we build

| Project | What it is | Status | License |
| --- | --- | --- | --- |
| **[Diatreme](https://github.com/MagmaMoose/diatreme)** | Your whole release spine as one GitHub Action. It computes the semantic version, cuts the tag, release and changelog, signs the release commit, promotes an already-scanned Docker image by digest, and ships a CycloneDX SBOM. Works on GitHub.com and Enterprise. | Live | MIT |
| **[Chargate](https://github.com/MagmaMoose/chargate)** | A security and lint gate built on MegaLinter that blocks only on the findings a pull request introduces. Inherited debt never blocks a merge, and the full SARIF still ships to DefectDojo. | Live | MIT |
| **[Dunmir](https://github.com/MagmaMoose/dunmir)** | Maintenance assurance for MikroTik RouterOS fleets. It proves that backups, config exports and updates actually happened and can be trusted, and fires a dead-man alert when an expected report goes missing. | In development | Apache-2.0 |
| **[Caldrith](https://github.com/MagmaMoose/caldrith)** | Configuration as code for GitHub. A self-hostable, multi-tenant App that reconciles your org and its repos against one `settings.yml`, and heals the drift when somebody changes a setting by hand. | In development | MIT |
| **[Brimyr](https://github.com/MagmaMoose/brimyr)** | A patch coverage gate. It detects the repo's ecosystem, runs the tests with coverage instrumentation on, and gates on the coverage of the lines the pull request actually changed. | In development | MIT |
| **[Securitybridge](https://github.com/MagmaMoose/securitybridge)** | A finding bus that syncs Dependency-Track and friends into DefectDojo, with zero-touch GitHub issue auto-push. | In development | MIT |
| **[Dastgate](https://github.com/MagmaMoose/dastgate)** | Scheduled DAST with OWASP ZAP and Nuclei against deployed environments, reimported into DefectDojo. | In development | MIT |

**Live** means released, documented and supported, so you can build on it today. **In development**
means it works and we run it ourselves, but there has been no public release, so expect the
interface to move, the docs to lag, and the odd rough edge. A public repository is not a promise
that something is finished. If you want to use one of these anyway, open an issue and say so,
because knowing somebody is out there changes what we prioritise.

Product pages and quickstarts live at [magmamoose.com](https://magmamoose.com).

There is more in the open if you go looking.
[agent-skills](https://github.com/MagmaMoose/agent-skills) holds the AI agent skills we share
across tools, [homebrew-tap](https://github.com/MagmaMoose/homebrew-tap) packages the CLIs, and
[github-usage](https://github.com/MagmaMoose/github-usage) turns GitHub usage reports into
something you can actually read.

## How we work

A handful of conventions hold across every repo in this org, so once you have contributed to one
you already know how the next one behaves.

- **Open core.** The thing that does the work is open source and stays that way. What we charge
  for is the hosted control plane and the operator UI on top of it.
- **Conventional commits, automated releases.** Every release is cut by Diatreme from the commit
  history. Nobody edits a version number or a changelog by hand.
- **Configuration as code.** Repository settings, rulesets and the shared workflows are reconciled
  by Caldrith from a single config file, rather than clicked into the GitHub UI.
- **Every pull request is gated.** Chargate blocks net-new security and lint findings, and every
  action is pinned to a commit SHA instead of a moving tag.

The full detail is in
[CONTRIBUTING.md](https://github.com/MagmaMoose/.github/blob/main/CONTRIBUTING.md).

## Getting in touch

- **Bugs and feature requests:** open an issue on the repo in question.
- **Security:** please do not use a public issue. Follow
  [our security policy](https://github.com/MagmaMoose/.github/blob/main/SECURITY.md) instead.
- **Anything else,** including commercial and Pro licensing: `caleb@magmamoose.com`.
