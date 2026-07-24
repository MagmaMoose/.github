<div align="center">

![Magma Moose. Platform, cloud, infrastructure, network and security.](https://raw.githubusercontent.com/MagmaMoose/.github/main/profile/assets/magma-moose-github-banner.png)

**Platform engineering and developer tooling that helps teams ship.**

[![Diatreme][b-diatreme]][diatreme] [![Chargate][b-chargate]][chargate] [![Dün Mir][b-dunmir]][dunmir] [![Caldrith][b-caldrith]][caldrith] [![Brimyr][b-brimyr]][brimyr] [![Dastgate][b-dastgate]][dastgate]

</div>

Magma Moose is a development studio. We started as hands-on contract engineering, helping teams
design, build and ship real systems, and over time we turned the tools we kept rebuilding into
products of their own. Today we do both. We take on platform, cloud, network and security
engineering, and we build and maintain our own tools, most of them open source.

The focus is the layer that makes everything else faster and safer to ship: CI/CD and release
automation, infrastructure as code, testing and code quality, GitHub automation and governance,
and the tooling growing up around AI agents.

## The tools

| Tool | What it does | Status | License |
| --- | --- | --- | --- |
| **[Diatreme][diatreme]** | Release orchestration. One GitHub Action for the whole release spine: semantic versioning, releases and changelogs, signed release commits, provenance-verified Docker promotion, and CycloneDX SBOMs. The same workflow for any versioning tool, on GitHub.com or Enterprise. | Live | MIT |
| **[Chargate][chargate]** | Security and lint gating. Built on MegaLinter, it fails a pull request only on the findings that pull request introduces. Pre-existing findings never block, and the full SARIF still ships to DefectDojo, Dependency-Track or the GitHub Security tab. | Live | MIT |
| **[Dün Mir][dunmir]** | Maintenance assurance for MikroTik RouterOS fleets. Proves the backups, exports and updates actually ran and can be trusted, and fires a dead-man alert when an expected report goes missing. | In development | Apache-2.0 |
| **[Caldrith][caldrith]** | GitHub configuration as code, continuously reconciled. A self-hostable, multi-tenant App that holds your org and its repos to one `settings.yml` and heals the drift when somebody changes a setting by hand. | In development | MIT |
| **[Brimyr][brimyr]** | Patch-coverage gating with SonarQube integration. It gates on the coverage of the lines a pull request changed, rather than on the coverage debt that pull request inherited. | In development | MIT |
| **[Dastgate][dastgate]** | Scheduled DAST for Kubernetes. OWASP ZAP and Nuclei against deployed environments, reimported into DefectDojo. | In development | MIT |

**Live** means released, documented and supported, so you can build on it today. **In development**
means it works and we run it ourselves, but there has been no public release, so expect rough edges
and lagging docs. A public repository is not a promise that something is finished. If you want to
use one of these anyway, open an issue and say so, because knowing somebody is out there changes
what we prioritise.

There is more in the open beyond the tools that carry a stone of their own.
[infra](https://github.com/MagmaMoose/infra) is unified infrastructure management,
[agent-skills](https://github.com/MagmaMoose/agent-skills) is one source of AI agent skills for
Claude, Codex and in-cluster agents, [homebrew-tap](https://github.com/MagmaMoose/homebrew-tap)
packages the CLIs, and [github-usage](https://github.com/MagmaMoose/github-usage) turns GitHub
usage reports into something you can actually read.

## Nothing held back

Every Magma Moose tool is open source and free to run. Read it, fork it, trust it. No key is
required to ship with it in production.

The open-source version is the whole tool. No features are fenced off, there is no trial clock,
and there is no paid tier waiting to unlock something you already need. We build these because we
kept hitting gaps we could not find a good answer to, we build them to our own standard, and then
we give them away.

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
  by Caldrith from a single config file, rather than clicked into the GitHub UI.
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
[dunmir]: https://github.com/MagmaMoose/dunmir
[caldrith]: https://github.com/MagmaMoose/caldrith
[brimyr]: https://github.com/MagmaMoose/brimyr
[dastgate]: https://github.com/MagmaMoose/dastgate

[b-diatreme]: https://img.shields.io/badge/Diatreme-D8330F?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPGcgZmlsbD0iI0ZCRjZFRiIgZmlsbC1ydWxlPSJldmVub2RkIiB0cmFuc2Zvcm09InNjYWxlKDEuMikiPjxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKC05LjUgMCkiIGQ9Ik0zMCAxOCBINTUgQyA3NiAxOCA4OSAzMiA4OSA1MCBDIDg5IDY4IDc2IDgyIDU1IDgyIEgzMCBaIE02MCAzMCBMNzcgNTAgTDYwIDcwIEw0MyA1MCBaIi8%2BPC9nPjwvc3ZnPg%3D%3D
[b-chargate]: https://img.shields.io/badge/Chargate-0E8A5A?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPGcgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjRkJGNkVGIiBzdHJva2Utd2lkdGg9IjEwIiBzdHJva2UtbGluZWNhcD0icm91bmQiPjxwYXRoIGQ9Ik0zMiAxMDIgVjQwIi8%2BPHBhdGggZD0iTTg4IDEwMiBWNDAiLz48cGF0aCBkPSJNMTggMzYgSDEwMiIvPjwvZz48cGF0aCBmaWxsPSIjRkJGNkVGIiBkPSJNNjAgNjIgTDc0IDc4IEw2MCA5NCBMNDYgNzggWiIvPjwvc3ZnPg%3D%3D
[b-dunmir]: https://img.shields.io/badge/D%C3%BCn%20Mir-1F5BD8?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPGVsbGlwc2UgZmlsbD0iI0ZCRjZFRiIgY3g9IjYwIiBjeT0iODkiIHJ4PSIzMSIgcnk9IjEyLjUiLz48ZWxsaXBzZSBmaWxsPSIjRkJGNkVGIiBjeD0iNjAiIGN5PSI2NCIgcng9IjIzIiByeT0iMTEiLz48ZWxsaXBzZSBmaWxsPSIjRkJGNkVGIiBjeD0iNjAiIGN5PSI0MiIgcng9IjE1IiByeT0iOS41Ii8%2BPGNpcmNsZSBmaWxsPSIjRkJGNkVGIiBjeD0iNjAiIGN5PSIyMyIgcj0iOCIvPjwvc3ZnPg%3D%3D
[b-caldrith]: https://img.shields.io/badge/Caldrith-C77800?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPGNpcmNsZSBmaWxsPSJub25lIiBzdHJva2U9IiNGQkY2RUYiIHN0cm9rZS13aWR0aD0iMTAiIGN4PSI2MCIgY3k9IjYwIiByPSIzNiIvPjxjaXJjbGUgZmlsbD0iI0ZCRjZFRiIgY3g9IjYwIiBjeT0iNjAiIHI9IjEzIi8%2BPC9zdmc%2B
[b-brimyr]: https://img.shields.io/badge/Brimyr-7C2BE0?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPGNpcmNsZSBmaWxsPSJub25lIiBzdHJva2U9IiNGQkY2RUYiIHN0cm9rZS13aWR0aD0iOCIgY3g9IjYwIiBjeT0iNjAiIHI9IjQwIi8%2BPHBhdGggZmlsbD0iI0ZCRjZFRiIgZD0iTTMxLjUgNzQgQTMxIDMxIDAgMCAwIDg4LjUgNzQgWiIvPjwvc3ZnPg%3D%3D
[b-dastgate]: https://img.shields.io/badge/Dastgate-0E7C8C?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMjAiIGhlaWdodD0iMTIwIiB2aWV3Qm94PSIwIDAgMTIwIDEyMCI%2BPGNpcmNsZSBmaWxsPSIjRkJGNkVGIiBjeD0iMzQiIGN5PSI4NiIgcj0iMTAiLz48ZyBmaWxsPSJub25lIiBzdHJva2U9IiNGQkY2RUYiIHN0cm9rZS13aWR0aD0iOSIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIj48cGF0aCBkPSJNNTIgNjggQSAyNS41IDI1LjUgMCAwIDEgNTkuNSA4NiIvPjxwYXRoIGQ9Ik02NiA1NCBBIDQ1LjMgNDUuMyAwIDAgMSA3OS4zIDg2Ii8%2BPHBhdGggZD0iTTgwIDQwIEEgNjUgNjUgMCAwIDEgOTkgODYiLz48L2c%2BPC9zdmc%2B
