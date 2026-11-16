---
title: Platform overview
---

# Platform overview

iNCRYPTO is a **digital asset platform**: a family of products that share one account, one wallet layer and one blockchain infrastructure we operate. Users see a single dashboard; merchants and partners integrate once and reach every product behind it.

## One infrastructure, many products

| Layer | What it does |
|---|---|
| **Blockchain infrastructure** | Full nodes operated by iNCRYPTO for Bitcoin, Litecoin, Ethereum, BNB Smart Chain, TRON and Monero; TON and the XRP Ledger through public network infrastructure for now. |
| **Wallet layer** | Multi-currency custody for users and merchants: deposit addresses, balances, transaction history, withdrawal controls. |
| **Exchange engine** | Crypto-to-crypto conversion. Each order is routed to a major trading venue and settled on-chain to the customer's address; we do not run an order book or a liquidity pool. |
| **Compliance** | AML/KYC policy today; automated screening of assets and counterparties (iNCRYPTO Shield) is in development. |
| **Investment products** | iNTRADE: systematic multi-strategy portfolios on perpetual futures, sized against a risk tier the user chooses. |
| **Product surfaces** | Web dashboard today; merchant tools, mobile wallets and a P2P market on the roadmap. |

## How we engineer

**Own chain infrastructure.** We run our own full nodes for six of our eight networks, so for them no external RPC provider sits between our users and the chain and no provider quota decides whether a deposit is seen. TON and the XRP Ledger use public network infrastructure until our own nodes are in place.

**Defense in depth.** Segregated key material, allow-listed settlement paths, secrets encrypted at rest and a structured audit trail across every service.

**Observability first.** Every critical path is instrumented. Alerts are edge-triggered, deduplicated and escalated to on-call operators — quiet channels stay trustworthy.

**Compliance by design.** Screening is being built into the flow itself (iNCRYPTO Shield, in development), not as a report generated afterwards.

**Built for a global audience.** The platform ships in 17 languages.

## Where things stand

The platform is in pre-launch hardening. Product statuses are kept current on the [Products](products.md) page; the [Changelog](../changelog.md) records what changes publicly.
