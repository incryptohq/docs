---
title: Security
---

# Security

iNCRYPTO operates financial infrastructure. Security is an engineering discipline here, not a checklist: the principles below shape how the platform is built and run.

## Principles

**Own the chain layer.** We run our own full nodes for Bitcoin, Litecoin, Ethereum, BNB Smart Chain, TRON and Monero, so deposit detection and withdrawal broadcast on those networks do not depend on a third-party provider's availability, quotas or honesty. TON and the XRP Ledger use public network infrastructure until our own nodes are in place.

**Segregate key material.** Keys that sign withdrawals are separated from application code and from the services that observe the chain. Secrets are encrypted at rest and never written to logs.

**Allow-list settlement paths.** Funds move only along paths that are configured in advance. A compromised component cannot invent a new destination.

**Screen before you settle.** Automated AML screening of deposits, withdrawals and merchant flows (iNCRYPTO Shield) is in development; it is designed to run as part of the transaction and hold flagged movements for review.

**Observe everything, alert rarely.** Every critical path is instrumented. Alerts are edge-triggered and deduplicated so operators trust the channel and act on it.

**Recover deterministically.** Backups are encrypted, verified by restoration, and every ledger-affecting process is designed to be replayable from its journal.

## Account security for users

- Two-factor authentication for sign-in and for sensitive actions.
- Withdrawal address controls and notifications for security-relevant events.
- Session management with device visibility.

## Reporting a vulnerability

We run a responsible disclosure programme. If you believe you have found a vulnerability in any iNCRYPTO service, please read the [disclosure policy](disclosure.md) and write to **security@incrypto.me**. Never report security issues through public channels.
