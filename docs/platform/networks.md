---
title: Networks & assets
---

# Networks & assets

iNCRYPTO operates its own full nodes for every network listed below. The exact list of tradable assets and the minimum amounts per direction are published in the product itself and may change; this page describes the network layer.

| Network | Native asset | Token standards | Notes |
|---|---|---|---|
| **Bitcoin** | BTC | — | Native SegWit addresses. |
| **Litecoin** | LTC | — | |
| **Ethereum** | ETH | ERC-20 | |
| **BNB Smart Chain** | BNB | BEP-20 | |
| **TRON** | TRX | TRC-20 | |
| **TON** | TON | — | |
| **XRP Ledger** | XRP | — | Destination tag required for deposits. |
| **Monero** | XMR | — | Private by design; subaddress per deposit. |

## Deposit detection

Deposits are detected by iNCRYPTO's own nodes and credited after the confirmation depth configured for each network. Confirmation depths balance finality against speed and are tuned per network; the current values are shown in the product at deposit time.

## Withdrawals

Withdrawals are broadcast from iNCRYPTO's own nodes. Every withdrawal passes AML screening and the account's security controls before it is signed.

!!! note "Adding a network"
    New networks are added when we can operate them to the same standard: our own full node, deterministic deposit detection, and a withdrawal path we control end-to-end.
