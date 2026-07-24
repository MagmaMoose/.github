<div align="center">

![Magma Moose. Small, sharp tools for teams that ship.](https://raw.githubusercontent.com/MagmaMoose/.github/main/profile/assets/banner.svg)

[![Diatreme][b-diatreme]][diatreme]
[![Chargate][b-chargate]][chargate]
[![Dunmir][b-dunmir]][dunmir]
[![Caldrith][b-caldrith]][caldrith]
[![Brimyr][b-brimyr]][brimyr]
[![Securitybridge][b-securitybridge]][securitybridge]
[![Dastgate][b-dastgate]][dastgate]

</div>

Magma Moose builds focused, open-core tools for the unglamorous parts of shipping software and
running infrastructure: the release spine, the maintenance you have to be able to trust. Free and
open at the core, with a paid layer where the work is worth paying for.

## Products

Each one does a single job properly. Open source at the core, hosted or Pro where it earns its
keep.

| Project | What it is | Status | License |
| --- | --- | --- | --- |
| **[Diatreme][diatreme]** | Your whole release spine as one GitHub Action: semantic versioning, releases, signed commits, provenance-verified Docker promotion and SBOMs, on GitHub.com or Enterprise. | Live | MIT |
| **[Chargate][chargate]** | A security and lint gate built on MegaLinter that blocks only on the findings a pull request introduces. Inherited debt never blocks a merge, and the full SARIF still ships to DefectDojo. | Live | MIT |
| **[Dunmir][dunmir]** | Maintenance assurance for MikroTik RouterOS fleets. Prove the backups, exports, and updates actually happened, and can be trusted, with dead-man alerts and a signed audit trail. | Preview | Apache-2.0 |
| **[Caldrith][caldrith]** | Configuration as code for GitHub. A self-hostable, multi-tenant App that reconciles your org and its repos against one `settings.yml`, and heals the drift when somebody changes a setting by hand. | In development | MIT |
| **[Brimyr][brimyr]** | A patch coverage gate. It detects the repo's ecosystem, runs the tests with coverage instrumentation on, and gates on the coverage of the lines the pull request actually changed. | In development | MIT |
| **[Securitybridge][securitybridge]** | A finding bus that syncs Dependency-Track and friends into DefectDojo, with zero-touch GitHub issue auto-push. | In development | MIT |
| **[Dastgate][dastgate]** | Scheduled DAST with OWASP ZAP and Nuclei against deployed environments, reimported into DefectDojo. | In development | MIT |

**Live** means released, documented and supported, so you can build on it today. **Preview** means
it is out and usable, with the interface still free to move before it settles. **In development**
means it works and we run it ourselves, but there has been no public release, so expect rough
edges and lagging docs. A public repository is not a promise that something is finished. If you
want to use one of these anyway, open an issue and say so, because knowing somebody is out there
changes what we prioritise.

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
- **Anything else,** including commercial and Pro licensing: `hello@magmamoose.com`.

[diatreme]: https://github.com/MagmaMoose/diatreme
[chargate]: https://github.com/MagmaMoose/chargate
[dunmir]: https://github.com/MagmaMoose/dunmir
[caldrith]: https://github.com/MagmaMoose/caldrith
[brimyr]: https://github.com/MagmaMoose/brimyr
[securitybridge]: https://github.com/MagmaMoose/securitybridge
[dastgate]: https://github.com/MagmaMoose/dastgate

[b-diatreme]: https://img.shields.io/badge/Diatreme-A855F7?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZmZmZiIgZD0iTTIuNSA5LjIgNi44IDMuNWgxMC40bDQuMyA1LjdMMTIgMjEuNXoiLz48L3N2Zz4%3D&logoColor=white
[b-chargate]: https://img.shields.io/badge/Chargate-A855F7?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZmZmZiIgZD0iTTEyIDIgMjAuNSA1LjJWMTFjMCA1LjQtMy42IDkuMi04LjUgMTFDNy4xIDIwLjIgMy41IDE2LjQgMy41IDExVjUuMnoiLz48L3N2Zz4%3D&logoColor=white
[b-dunmir]: https://img.shields.io/badge/Dunmir-8B5CF6?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZmZmZiIgZD0iTTcuNSAzaDlsNCA0LjV2OWwtNCA0LjVoLTlsLTQtNC41di05eiIvPjwvc3ZnPg%3D%3D&logoColor=white
[b-caldrith]: https://img.shields.io/badge/Caldrith-3D2A63?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZmZmZiIgZD0iTTEyIDIgMjAuNSA3djEwTDEyIDIyIDMuNSAxN1Y3eiIvPjwvc3ZnPg%3D%3D&logoColor=white
[b-brimyr]: https://img.shields.io/badge/Brimyr-3D2A63?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPGNpcmNsZSBmaWxsPSIjZmZmZmZmIiBjeD0iMTIiIGN5PSIxMiIgcj0iOS41Ii8%2BPC9zdmc%2B&logoColor=white
[b-securitybridge]: https://img.shields.io/badge/Securitybridge-3D2A63?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZmZmZiIgZD0iTTEyIDMgMjEuNSAxOS41aC0xOXoiLz48L3N2Zz4%3D&logoColor=white
[b-dastgate]: https://img.shields.io/badge/Dastgate-3D2A63?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZmZmZiIgZD0iTTEyIDIuNSAxOS41IDEzYTcuNSA3LjUgMCAxIDEtMTUgMHoiLz48L3N2Zz4%3D&logoColor=white
