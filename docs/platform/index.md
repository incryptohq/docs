---
title: Platform overview
---

# Platform overview

iNCRYPTO is a **digital asset platform**: a family of products that share one account, one wallet layer and one self-hosted blockchain infrastructure. Users see a single dashboard; merchants and partners integrate once and reach every product behind it.

## One infrastructure, many products

| Layer | What it does |
|---|---|
| **Blockchain infrastructure** | Full nodes for every supported network, operated by iNCRYPTO. Deposits are detected and withdrawals are broadcast without a third-party RPC provider in the path. |
| **Wallet layer** | Multi-currency custody for users and merchants: deposit addresses, balances, transaction history, withdrawal controls. |
| **Exchange engine** | Instant crypto-to-crypto conversion with in-house liquidity and transparent rates. |
| **Compliance** | AML screening of assets and counterparties built into the transaction flow. |
| **Investment products** | iNTRADE: systematic multi-strategy portfolios on perpetual futures, sized against a risk tier the user chooses. |
| **Product surfaces** | Web dashboard today; merchant tools, mobile wallets and a P2P market on the roadmap. |

## How we engineer

**Self-hosted chain infrastructure.** We run our own full nodes for every supported network. No external RPC provider sits between our users and the chain, and no provider quota decides whether a deposit is seen.

**Defense in depth.** Segregated key material, allow-listed settlement paths, secrets encrypted at rest and a structured audit trail across every service.

**Observability first.** Every critical path is instrumented. Alerts are edge-triggered, deduplicated and escalated to on-call operators — quiet channels stay trustworthy.

**Compliance by design.** Screening is part of the flow, not a report generated afterwards.

**Built for a global audience.** The platform ships in 17 languages.

## Where things stand

The platform is in pre-launch hardening. Product statuses are kept current on the [Products](products.md) page; the [Changelog](../changelog.md) records what changes publicly.
