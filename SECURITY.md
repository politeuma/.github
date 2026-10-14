# Security policy

This policy applies to all repositories in the politeuma org.

## Reporting a vulnerability

**Do not open a public issue.** Report privately via GitHub's
*Report a vulnerability* (Security tab) on the affected repository, or
contact a maintainer directly.

Include: what is affected, what an attacker can do with it, and steps to
reproduce if you have them. We will acknowledge receipt promptly and keep
you informed while we fix it.

## Scope notes

- The highest-impact targets are supply-chain paths: template post-gen
  hooks, GitHub Actions (pinned by hash; see the reusable workflows), and
  published packages.
- Legal content (wrong article, stale review date) is a *correctness* bug,
  not a security vulnerability — file it as a grounding proposal, not a
  security report.
- Our own CI runs zizmor on workflows; PRs that touch
  `.github/workflows/` get extra scrutiny.
