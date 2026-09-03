---
title: Vulnerability disclosure
---

# Vulnerability disclosure policy

Every security report is treated as a priority, and we value the work of researchers who help keep our users safe.

## Reporting a vulnerability

**Please do not open public issues, pull requests or discussions for security matters.**

Report privately through either channel:

- **Email:** [security@incrypto.me](mailto:security@incrypto.me)
- **GitHub:** *Report a vulnerability* in the **Security** tab of any public [incryptohq](https://github.com/incryptohq) repository

A useful report includes: the affected service or domain, steps to reproduce, a proof of concept, your assessment of the impact, and a way to reach you for follow-up.

## What to expect

| Stage | Target |
|---|---|
| Acknowledgement | within 2 business days |
| Initial assessment and severity | within 5 business days |
| Status updates | at every material change, at least every 10 business days |
| Fix | driven by severity; critical issues are treated as incidents and worked continuously |
| Credit | on request, after the fix is released |

## Scope

**In scope**

- Production services under `incrypto.me` and its subdomains
- Public repositories in the `incryptohq` organization

**Out of scope**

- Denial-of-service, volumetric or rate-limit testing
- Social engineering, phishing or physical attacks against staff, users or facilities
- Third-party services we integrate with (blockchain networks, liquidity venues, hosting, email providers)
- Vulnerabilities in third-party dependencies without a demonstrated impact on iNCRYPTO
- Output of automated scanners without a working proof of concept
- Missing best-practice headers, flags or configuration without demonstrable impact
- Self-XSS, clickjacking on pages without sensitive actions, and issues requiring an already-compromised device or network

## Rules of engagement

- Test only against accounts you own or are explicitly authorised to use.
- Do not access, modify, delete or exfiltrate data that is not yours. If you encounter user data, stop and report immediately.
- Do not degrade the service for other users.
- Do not disclose a vulnerability publicly until we have fixed it and agreed on a disclosure date. We aim for coordinated disclosure within 90 days of the report.

## Safe harbour

We consider security research conducted in good faith and in accordance with this policy to be authorised. We will not pursue legal action against researchers who follow these rules, and we will work with you if a third party raises a concern about research done under this policy.

## Rewards

We do not run a public bug bounty programme at this time. Significant findings may be rewarded at our discretion.
