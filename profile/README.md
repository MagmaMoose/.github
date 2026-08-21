<div align="center">

![Magma Moose. Platform, cloud, infrastructure, network and security.](https://raw.githubusercontent.com/MagmaMoose/.github/main/profile/assets/magma-moose-github-banner.png)

[![Diatreme][b-diatreme]][diatreme] [![Chargate][b-chargate]][chargate] [![Brimyr][b-brimyr]][brimyr] [![Draventis][b-draventis]][draventis] [![Ponvara][b-ponvara]][ponvara] [![Tremvok][b-tremvok]][tremvok]

</div>

Magma Moose is a development studio. We started as hands-on contract engineering, helping teams
design, build and ship real systems, and over time we turned the tools we kept rebuilding into
products of their own. Today we do both. We take on platform, cloud, network and security
engineering, and we build and maintain our own tools, most of them open source.

The focus is the layer that makes everything else faster and safer to ship: CI/CD and release
automation, infrastructure as code, testing and code quality, and GitHub automation and
governance.

## The tools

| Tool | What it does | Status | License |
| --- | --- | --- | --- |
| **[Diatreme][diatreme]** | Release orchestration. One GitHub Action for the whole release spine: semantic versioning, releases and changelogs, signed release commits, provenance-verified Docker promotion, and CycloneDX SBOMs. The same workflow for any versioning tool, on GitHub.com or Enterprise. | Live | Apache-2.0 |
| **[Chargate][chargate]** | Security and lint gating. Built on MegaLinter, it fails a pull request only on the findings that pull request introduces. Pre-existing findings never block, and the full SARIF still ships to DefectDojo, Dependency-Track or the GitHub Security tab. | Live | Apache-2.0 |
| **[Brimyr][brimyr]** | Patch-coverage gating with SonarQube integration. It gates on the coverage of the lines a pull request changed, rather than on the coverage debt that pull request inherited. | In development | Apache-2.0 |
| **[Draventis][draventis]** | Scheduled DAST for Kubernetes. OWASP ZAP and Nuclei against deployed environments, reimported into DefectDojo. | In development | Apache-2.0 |
| **[Ponvara][ponvara]** | Security finding bus. Pulls findings from scanners that can't reach DefectDojo themselves — starting with Dependency-Track — reimports them, and auto-opens GitHub issues for the High and Critical ones. | In development | Apache-2.0 |
| **[Tremvok][tremvok]** | Deployment orchestration and notifications — the deploy-side counterpart to Diatreme, driving the deploy where Diatreme drives the release. | Planned | Apache-2.0 |

**Live** means released, documented and supported, so you can build on it today. **In development**
means it works and we run it ourselves, but there has been no public release, so expect rough edges
and lagging docs. **Planned** means it has a repo and a stone but is still being scoped. A public repository is not a promise that something is finished. If you want to
use one of these anyway, open an issue and say so, because knowing somebody is out there changes
what we prioritise.

There is more in the open beyond the tools that carry a stone of their own.
[infra](https://github.com/MagmaMoose/infra) is unified infrastructure management,
[charts](https://github.com/MagmaMoose/charts) is the shared Helm charts,
[homebrew-tap](https://github.com/MagmaMoose/homebrew-tap) packages the CLIs, and
[agent-skills](https://github.com/MagmaMoose/agent-skills) is one source of AI agent skills for
Claude, Codex and in-cluster agents.

## Working with us

The other half of the business is engineering. Platform and DevOps, cloud, infrastructure as code,
network, security, and monitoring and observability. Hands-on, from architecture to production,
either run end to end for you or alongside the engineers you already have.

Details are at [magmamoose.com/services](https://magmamoose.com/services/), or just email us.

## How we build

A handful of conventions hold across every repo here, so once you have contributed to one you
already know how the next one behaves.

- **Conventional commits, automated releases.** Every release is cut by Diatreme from the commit
  history. Nobody edits a version number or a changelog by hand.
- **Configuration as code.** Repository settings, rulesets and the shared workflows are reconciled
  from a single config file, rather than clicked into the GitHub UI.
- **Every pull request is gated.** Chargate blocks net-new security and lint findings, and every
  action is pinned to a commit SHA instead of a moving tag.

The full detail is in
[CONTRIBUTING.md](https://github.com/MagmaMoose/.github/blob/main/CONTRIBUTING.md).

## Getting in touch

- **Bugs and feature requests:** open an issue on the repo in question.
- **Security:** please do not use a public issue. Follow
  [our security policy](https://github.com/MagmaMoose/.github/blob/main/SECURITY.md) instead.
- **Engineering work, or anything else:** `hello@magmamoose.com`, or find us on
  [LinkedIn](https://www.linkedin.com/company/magmamoose).

<div align="center">

Built in the open. Forged on GitHub.

</div>

[diatreme]: https://github.com/MagmaMoose/diatreme
[chargate]: https://github.com/MagmaMoose/chargate
[brimyr]: https://github.com/MagmaMoose/brimyr
[draventis]: https://github.com/MagmaMoose/draventis
[ponvara]: https://github.com/MagmaMoose/ponvara
[tremvok]: https://github.com/MagmaMoose/tremvok

[b-diatreme]: https://img.shields.io/badge/Diatreme-D8330F?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPGcgZmlsbD0iI0ZCRjZFRiIgZmlsbC1ydWxlPSJldmVub2RkIiB0cmFuc2Zvcm09InNjYWxlKDEuMikiPjxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKC05LjUgMCkiIGQ9Ik0zMCAxOCBINTUgQyA3NiAxOCA4OSAzMiA4OSA1MCBDIDg5IDY4IDc2IDgyIDU1IDgyIEgzMCBaIE02MCAzMCBMNzcgNTAgTDYwIDcwIEw0MyA1MCBaIi8%2BPC9nPjwvc3ZnPg%3D%3D
[b-chargate]: https://img.shields.io/badge/Chargate-0E8A5A?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPGcgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjRkJGNkVGIiBzdHJva2Utd2lkdGg9IjEwIiBzdHJva2UtbGluZWNhcD0icm91bmQiPjxwYXRoIGQ9Ik0zMiAxMDIgVjQwIi8%2BPHBhdGggZD0iTTg4IDEwMiBWNDAiLz48cGF0aCBkPSJNMTggMzYgSDEwMiIvPjwvZz48cGF0aCBmaWxsPSIjRkJGNkVGIiBkPSJNNjAgNjIgTDc0IDc4IEw2MCA5NCBMNDYgNzggWiIvPjwvc3ZnPg%3D%3D
[b-brimyr]: https://img.shields.io/badge/Brimyr-7C2BE0?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPGNpcmNsZSBmaWxsPSJub25lIiBzdHJva2U9IiNGQkY2RUYiIHN0cm9rZS13aWR0aD0iOCIgY3g9IjYwIiBjeT0iNjAiIHI9IjQwIi8%2BPHBhdGggZmlsbD0iI0ZCRjZFRiIgZD0iTTMxLjUgNzQgQTMxIDMxIDAgMCAwIDg4LjUgNzQgWiIvPjwvc3ZnPg%3D%3D
[b-draventis]: https://img.shields.io/badge/Draventis-7A0B22?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPGNpcmNsZSBmaWxsPSIjRkJGNkVGIiBjeD0iMzQiIGN5PSI4NiIgcj0iMTAiLz48ZyBmaWxsPSJub25lIiBzdHJva2U9IiNGQkY2RUYiIHN0cm9rZS13aWR0aD0iOSIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIj48cGF0aCBkPSJNNTIgNjggQSAyNS41IDI1LjUgMCAwIDEgNTkuNSA4NiIvPjxwYXRoIGQ9Ik02NiA1NCBBIDQ1LjMgNDUuMyAwIDAgMSA3OS4zIDg2Ii8%2BPHBhdGggZD0iTTgwIDQwIEEgNjUgNjUgMCAwIDEgOTkgODYiLz48L2c%2BPC9zdmc%2B
[b-ponvara]: https://img.shields.io/badge/Ponvara-0E7C8C?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPHBhdGggZmlsbD0ibm9uZSIgc3Ryb2tlPSIjRkJGNkVGIiBzdHJva2Utd2lkdGg9IjkiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgZD0iTTE4IDc0IFE2MCAtNiAxMDIgNzQiLz48cmVjdCB4PSIxMiIgeT0iNzAiIHdpZHRoPSI5NiIgaGVpZ2h0PSI5IiByeD0iMyIgZmlsbD0iI0ZCRjZFRiIvPjxnIGZpbGw9Im5vbmUiIHN0cm9rZT0iI0ZCRjZFRiIgc3Ryb2tlLXdpZHRoPSI1IiBzdHJva2UtbGluZWNhcD0icm91bmQiPjxwYXRoIGQ9Ik0zOCA0NCBWNzAiLz48cGF0aCBkPSJNNjAgMzMgVjcwIi8%2BPHBhdGggZD0iTTgyIDQ0IFY3MCIvPjwvZz48ZyBmaWxsPSIjRkJGNkVGIj48cmVjdCB4PSIxNSIgeT0iNzkiIHdpZHRoPSI5IiBoZWlnaHQ9IjIwIiByeD0iMiIvPjxyZWN0IHg9Ijk2IiB5PSI3OSIgd2lkdGg9IjkiIGhlaWdodD0iMjAiIHJ4PSIyIi8%2BPC9nPjwvc3ZnPg%3D%3D
[b-tremvok]: https://img.shields.io/badge/Tremvok-5C7A12?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPHBhdGggZmlsbD0iI0ZCRjZFRiIgZD0iTTI2IDUyIEg5NCBMNzYgMjQgSDQ0IFoiLz48cGF0aCBmaWxsPSJub25lIiBzdHJva2U9IiNGQkY2RUYiIHN0cm9rZS13aWR0aD0iOSIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgZD0iTTI2IDcyIEg5NCBMNzYgMTAwIEg0NCBaIi8%2BPHBhdGggZmlsbD0ibm9uZSIgc3Ryb2tlPSIjRkJGNkVGIiBzdHJva2Utd2lkdGg9IjgiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgZD0iTTE0IDYyIEgxMDYiLz48L3N2Zz4%3D
