# Security Policy

Magma Moose builds tools that sit inside other people's release pipelines and networks, so we take
reports seriously and we would rather hear about a problem early and awkwardly than late and
politely.

This policy covers every repository in the [Magma Moose](https://github.com/MagmaMoose)
organization unless that repository ships its own `SECURITY.md`.

## Reporting a vulnerability

**Please do not open a public issue, pull request or discussion for a security problem.**

Use GitHub's private vulnerability reporting, which is enabled on every repo in the org. Go to the
affected repository, open the **Security** tab, and choose **Report a vulnerability**. That opens
a private thread visible only to you and the maintainers, and it is the fastest route to someone
who can fix it.

If you cannot use that form, or the issue spans several repositories, email
**caleb@magmamoose.com** with `SECURITY` in the subject line. If you would prefer to encrypt the
report, say so in a first message with no detail in it and we will arrange a channel.

### What to include

The more of this you can give us, the faster this goes:

- Which project and which version, tag or commit.
- What an attacker can actually do, in one or two sentences.
- The steps to reproduce it, ideally as a minimal repository, workflow file or request.
- Anything you know about affected configurations, since a finding that only fires with a
  non-default setting is a different severity to one that fires out of the box.
- Whether you have told anyone else, and whether you have a disclosure deadline in mind.

Please do not run automated scanners against our hosted services. If you need to test against a
live endpoint to demonstrate something, contact us first and we will work out how.

## What happens next

We are a small team, so here is what we can honestly commit to.

- **Acknowledgement within 3 business days.** If you have not heard anything by then, assume the
  message went astray and chase it by email.
- **An initial assessment within 10 business days**, covering whether we can reproduce it, what
  severity we think it is, and roughly when a fix will land.
- **Regular updates** while we work on it, without you having to ask.
- **A fix released as soon as it is ready**, followed by a
  [GitHub Security Advisory](https://github.com/MagmaMoose) with a CVE where one is warranted.

We will credit you in the advisory under whatever name or handle you want, or leave you out of it
entirely if you prefer. Tell us which.

## Scope

In scope:

- The source code of any public repository in this organization.
- The published artefacts they produce, which includes the Diatreme GitHub Action on the
  Marketplace, the container images on GHCR, the Helm charts, and the Homebrew formulae.
- The hosted services those products depend on, which currently means the Diatreme token broker
  and GitHub App, the Dunmir control plane at `dunmir.magmamoose.com`, and the Caldrith GitHub
  App.
- `magmamoose.com` and its subdomains.

Out of scope, unless you can show real impact:

- Volumetric denial of service, load testing, and anything that degrades service for other users.
- Social engineering of our people, our customers, or our suppliers, and physical attacks.
- Missing hardening headers, cookie flags or TLS configuration on static pages, with no attack
  attached to them.
- Vulnerable dependency versions reported from a scanner with no reachable path through our code.
- Self-XSS, clickjacking on pages with no state-changing action, and issues that need a fully
  compromised device or an already-privileged account to work.
- Findings in third party services we merely use, which belong with that vendor.

## Supported versions

We support the current release of each project. Fixes land on the default branch and go out in the
next release, which for most repos is minutes later because releases are automated.

There are no long-term support branches and we do not backport to older majors. If you are pinned
to an old major and cannot move, say so in your report and we will talk about it, but the default
answer is that the fix ships forward.

Everything in this org is versioned semantically, so a security fix is a patch release unless
fixing it properly requires a breaking change, in which case the advisory will say so plainly.

## Safe harbour

If you make a good faith effort to follow this policy, we will treat your research as authorised,
we will not pursue or support legal action against you over it, and we will work with you to
understand and fix the issue quickly.

Good faith here means you avoid privacy violations, you do not destroy or modify data that is not
yours, you do not degrade our services for other people, and you give us reasonable time to fix
the problem before you talk about it publicly. If you are ever unsure whether something crosses
that line, ask first.
