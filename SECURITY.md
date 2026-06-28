# Security Policy

[Sites.Reviews](https://sites.reviews) is a **trust and security** brand — we
help people decide who to trust online and run scam/security checks on websites.
We hold our own software to the same standard. We deeply appreciate responsible
disclosure and will work with you to verify, fix, and credit any legitimate
report.

This is the **organization-wide** security policy for the
[SitesReviewsTrust](https://github.com/SitesReviewsTrust) organization. It
applies to every repository that does not publish its own `SECURITY.md`.

---

## How to report a vulnerability

**Please report security issues privately via GitHub — do not open a public
issue, pull request, or discussion for anything security-sensitive.** Public
disclosure before a fix puts users at risk.

To report:

1. Go to the **affected repository** on GitHub
   (e.g. [`sites-reviews-api`](https://github.com/SitesReviewsTrust/sites-reviews-api),
   [`sites-reviews-mcp`](https://github.com/SitesReviewsTrust/sites-reviews-mcp),
   [`sites-reviews-extension`](https://github.com/SitesReviewsTrust/sites-reviews-extension),
   or [`sites-reviews-docs`](https://github.com/SitesReviewsTrust/sites-reviews-docs)).
2. Open the **Security** tab.
3. Click **Report a vulnerability** (GitHub Private Vulnerability Reporting /
   Security Advisories).
4. Fill in the form with as much detail as you can — see
   [What to include](#what-to-include).

This routes your report privately to the maintainers and gives us a tracked,
confidential channel (a draft GitHub Security Advisory) to coordinate the fix
with you.

If you are unsure which repository is affected, file against
[`sites-reviews-api`](https://github.com/SitesReviewsTrust/sites-reviews-api/security/advisories/new)
and we will route it.

> **Non-sensitive contact only:** for general security questions that are *not*
> a live vulnerability (e.g. "is X in scope?"), you may reach us via the Telegram
> bot [@SitesReviews_bot](https://t.me/SitesReviews_bot). **Never** put exploit
> details, proof-of-concept, or sensitive data in Telegram — use GitHub private
> reporting for anything that could be abused.

## What to include

A good report helps us reproduce and fix faster. Where possible, include:

- The **repository / component** and version, commit, or URL affected.
- A clear **description** of the issue and its **impact**.
- **Steps to reproduce** or a minimal proof-of-concept.
- Affected **endpoints, parameters, or configuration**.
- Any relevant logs, requests/responses, or screenshots (redact secrets).
- Your assessment of **severity** and suggested remediation, if you have one.

## Scope

The following are **in scope**:

| Component | Where |
|---|---|
| **Public read API** | `https://sites.reviews/api/public/v1` |
| **MCP server** | [`sites-reviews-mcp`](https://github.com/SitesReviewsTrust/sites-reviews-mcp) |
| **Browser extension** | [`sites-reviews-extension`](https://github.com/SitesReviewsTrust/sites-reviews-extension) · [install](https://sites.reviews/extension) |
| **Website** | [`sites.reviews`](https://sites.reviews) |
| **Embeddable widget & data access** | [`sites-reviews-api`](https://github.com/SitesReviewsTrust/sites-reviews-api) |
| **Documentation hub** | [`sites-reviews-docs`](https://github.com/SitesReviewsTrust/sites-reviews-docs) |

Examples of issues we want to hear about: authentication/authorization flaws,
injection (SQL/command/template), SSRF, XSS, CSRF, insecure direct object
references, secrets exposure, supply-chain/dependency vulnerabilities, broken
access control on the public API, and anything that could be used to manipulate
trust scores or reviews data.

**Out of scope** (please don't report these):

- Findings from automated scanners without a demonstrated, exploitable impact.
- Volumetric **DoS/DDoS** or brute-force/rate-limit testing against production.
- Social engineering, phishing, or physical attacks against staff or users.
- Missing security headers or best-practice suggestions with no concrete impact.
- Reports about third-party services we don't control.
- Vulnerabilities requiring a rooted/jailbroken device or a compromised browser.

## Rules of engagement

When researching, please:

- **Use only your own accounts and test data.** Do not access, modify, or
  exfiltrate data that isn't yours.
- **Do not degrade service** — no DoS, no automated high-volume fuzzing against
  production. The public API at `https://sites.reviews/api/public/v1` is for
  legitimate, rate-respecting use.
- **Do not manipulate live trust scores, ratings, or reviews** to demonstrate an
  issue — describe the vector instead, or use a clearly-marked test entry.
- **Stop and report** as soon as you confirm a vulnerability; don't pivot
  deeper than necessary to prove impact.
- Give us **reasonable time to remediate** before any public disclosure.

Good-faith research conducted under these rules is welcome; we will not pursue
or support legal action against researchers who follow this policy.

## Our commitment & response targets

We aim to:

| Stage | Target |
|---|---|
| **Acknowledge** your report | within **3 business days** |
| **Triage & validate** (severity, scope) | within **7 business days** |
| **Provide a remediation plan / timeline** | within **14 business days** |
| **Ship a fix** | as fast as severity warrants — critical issues are prioritized |

We will keep you updated through the GitHub advisory, coordinate a disclosure
timeline with you, and — with your permission — **credit you** in the published
advisory. We do not currently run a paid bug-bounty program, but we genuinely
value and acknowledge your work.

## Supported versions

Unless a repository states otherwise, security fixes target the **latest
released version** and the **default branch**. For hosted components — the
public API, website, and trust engine — the running production version is always
the supported one.

---

Thank you for helping keep Sites.Reviews and its users safe. 🛡️
