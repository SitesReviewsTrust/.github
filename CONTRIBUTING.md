# Contributing to Sites.Reviews

First off — thank you for taking the time to contribute. 🙌

[Sites.Reviews](https://sites.reviews) is an independent catalog of company and
website reviews and trust ratings. Because we are a **trust and reputation**
brand, the quality and integrity of our code, data, and community matter a great
deal. This guide explains how to file issues, propose changes, and get a pull
request merged across any repository in the
[SitesReviewsTrust](https://github.com/SitesReviewsTrust) organization.

This is an **organization-wide** guide. Some repositories add their own
`CONTRIBUTING.md` with stack-specific build/test instructions — when present,
that repo-local guide takes precedence over this one.

---

## Table of contents

- [Code of Conduct](#code-of-conduct)
- [The ecosystem](#the-ecosystem)
- [Ways to contribute](#ways-to-contribute)
- [Filing a good issue](#filing-a-good-issue)
- [Proposing a change](#proposing-a-change)
- [Pull request checklist](#pull-request-checklist)
- [Commit & branch conventions](#commit--branch-conventions)
- [Code style](#code-style)
- [Reporting security issues](#reporting-security-issues)
- [Getting help](#getting-help)

---

## Code of Conduct

All participation is governed by our
[Code of Conduct](./CODE_OF_CONDUCT.md). By contributing you agree to uphold it.
In short: be kind, be honest, and never use this community to coordinate review
manipulation, defamation, or any deceptive practice.

## The ecosystem

Our open-source work is split across a few focused repositories. Open your issue
or PR against the one that fits — and if you are not sure, open it anyway and a
maintainer will move it.

| Repo | What it is | Typical stack |
|---|---|---|
| **[sites-reviews-mcp](https://github.com/SitesReviewsTrust/sites-reviews-mcp)** | MCP server that lets AI assistants (Claude & co.) look up website trust scores & reviews | TypeScript / Node |
| **[sites-reviews-api](https://github.com/SitesReviewsTrust/sites-reviews-api)** | Public data access (schema.org JSON-LD) & embeddable reviews widget | TypeScript / Node |
| **[sites-reviews-docs](https://github.com/SitesReviewsTrust/sites-reviews-docs)** | Documentation hub for the whole ecosystem | Markdown / docs site |
| **[sites-reviews-extension](https://github.com/SitesReviewsTrust/sites-reviews-extension)** | Browser extension showing a Trust Score on any site you visit · [install](https://sites.reviews/extension) | TypeScript / WebExtension |

The public read API is live at `https://sites.reviews/api/public/v1` and is the
data source most integrations build on.

## Ways to contribute

You don't have to write code to help:

- 🐞 **Report a bug** — use the issue forms below.
- 💡 **Suggest a feature** or improvement.
- 📖 **Improve documentation** in
  [sites-reviews-docs](https://github.com/SitesReviewsTrust/sites-reviews-docs).
- 🌐 **Flag data quality issues** — wrong/duplicate listings, stale trust
  signals, or suspected review manipulation (for the latter, see
  [SECURITY.md](./SECURITY.md) if it could be abused).
- 🧪 **Triage** — reproduce open issues and add detail.

> **Reviews & ratings data:** the catalog itself is curated on
> [sites.reviews](https://sites.reviews). To dispute or correct a specific
> listing or rating, use the website or [@SitesReviews_bot](https://t.me/SitesReviews_bot)
> rather than a code-repo issue.

## Filing a good issue

Before opening an issue:

1. **Search existing issues** (open and closed) to avoid duplicates.
2. **Pick the right repo** from the table above.
3. **Use the issue form** — Bug report or Feature request — and fill in every
   field. Reproduction steps and expected vs. actual behavior are what let us
   fix things fast.
4. For anything that could be a vulnerability, **do not open a public issue** —
   follow [SECURITY.md](./SECURITY.md).

## Proposing a change

1. **Discuss first for anything non-trivial.** Open an issue (or a
   [Discussion](https://github.com/orgs/SitesReviewsTrust/discussions)) describing
   the problem and your proposed approach before writing a large PR. This avoids
   wasted work.
2. **Fork** the repo and create a topic branch from the default branch.
3. Make focused commits — one logical change per PR is much easier to review.
4. **Add or update tests** for any behavior change.
5. **Update docs** when you change behavior, config, or public APIs.
6. Open the PR using the [pull request template](./.github/PULL_REQUEST_TEMPLATE.md)
   and link the issue it resolves (`Closes #123`).

## Pull request checklist

A PR is ready for review when:

- [ ] It targets the correct repository and the default branch.
- [ ] It is scoped to a single concern.
- [ ] **CI is green** — all checks (build, lint, type-check, tests) pass.
- [ ] New/changed behavior is covered by tests.
- [ ] Documentation is updated where relevant.
- [ ] No secrets, credentials, tokens, or `.env` files are committed.
- [ ] The PR description explains *what* changed and *why*, and links the issue.

> Maintainers cannot merge a PR with failing CI. If a check is flaky, say so in
> the PR and a maintainer will re-run it.

## Commit & branch conventions

- **Branches:** `feature/<short-description>`, `fix/<short-description>`,
  `docs/<short-description>`, or `chore/<short-description>`.
- **Commits:** we prefer
  [Conventional Commits](https://www.conventionalcommits.org/) —
  e.g. `fix(api): handle missing domain in trust lookup`. This keeps history
  readable and helps automate changelogs.
- Keep the subject line ≤ 72 chars and use the body to explain *why*.

## Code style

- **Formatting/linting is automated.** Run the repo's formatter and linter
  before pushing (typically `npm run lint` / `npm run format`, or
  `prettier`/`eslint`). CI enforces the same rules — match the existing config,
  don't introduce a new style.
- **TypeScript** is preferred for new code in the MCP server, API, and
  extension. Keep types explicit at public boundaries.
- **Small, readable functions.** Favor clarity over cleverness.
- **No dead code or commented-out blocks** in merged PRs.
- **Don't reformat unrelated files** — keep diffs reviewable.

## Reporting security issues

**Never report a vulnerability in a public issue or PR.** Use GitHub private
vulnerability reporting on the affected repo and follow our
[Security Policy](./SECURITY.md).

## Getting help

- 📖 **Docs** — [sites-reviews-docs](https://github.com/SitesReviewsTrust/sites-reviews-docs)
- 💬 **Discussions** — [SitesReviewsTrust discussions](https://github.com/orgs/SitesReviewsTrust/discussions)
- 🤖 **Telegram** — [@SitesReviews_bot](https://t.me/SitesReviews_bot)
- 🌐 **Website** — [sites.reviews](https://sites.reviews)

See [SUPPORT.md](./SUPPORT.md) for the full list of support channels.

---

Thanks again for helping make the web more trustworthy. 💙
