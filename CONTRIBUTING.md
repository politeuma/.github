# Contributing to politeuma

## How to contribute

- **Pull requests are welcome.** Open a PR directly; if discussion is
  needed first, link an issue from the PR (no pre-approval required).
- **PR titles** must follow [Conventional Commits](https://www.conventionalcommits.org/)
  (`docs:`, `fix:`, `feat:`, `chore:` …). Only the title is checked —
  squash-merge keeps history tidy.
- **One idea per PR**, with tests for behavior changes.

## Language

Canonical language is English; a maintained Japanese translation ships
alongside. Write the English first, then add (or request help with) the
Japanese. Machine-translated JA is acceptable as a starting point if you
say so in the PR.

## Legal content

- Cite primary sources with pinpoint citations; never cite a search-result
  snippet or a secondary summary as the authority.
- Every rule shows its sources and the date it was last checked.
- **Reviews are not legal advice.** If you review legal content, you share
  your understanding in good faith; that is not legal advice to anyone.
  You may contribute without naming any employer or affiliation.
- Quote the [canonical disclaimer](profile/disclaimer.md); do not
  paraphrase it, and never call anything "compliant".

## Names

Repository and tool names are frozen. New components get a descriptive
subtitle (see the per-repo subtitles in the
[profile README](profile/README.md)). CI rejects the old names
<!-- no-old-names-allow: the forbidden-name list itself --> (`ConstitutiveTemplates`, `kasi-x`, `python-copier-template`, `foundry`,
`law-lint`, `codex`, `good-future-codex`, `orimono`) <!-- no-old-names-allow: continued --> — do not reintroduce
them, even in jest.

## Checks

Repos use the shared reusable workflows (lint + test, no-old-names
check). Run the repo's own checks (just/task/pytest/ruff as documented in
its README) before pushing.
