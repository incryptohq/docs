---
title: Networks & assets
---

# Networks & assets

iNCRYPTO operates its own full nodes for Bitcoin, Litecoin, Ethereum, BNB Smart Chain, TRON and Monero. TON and the XRP Ledger are read and written through public network infrastructure today; running our own nodes for them is on the roadmap. The exact list of tradable assets and the minimum amounts per direction are published in the product itself and may change; this page describes the network layer.

| Network | Native asset | Token standards | Notes |
|---|---|---|---|
| **Bitcoin** | BTC | — | Native SegWit addresses. |
| **Litecoin** | LTC | — | |
| **Ethereum** | ETH | ERC-20 | |
| **BNB Smart Chain** | BNB | BEP-20 | |
| **TRON** | TRX | TRC-20 | |
| **TON** | GRAM | Jettons (USDT) | The network's native coin is shown as GRAM. |
| **XRP Ledger** | XRP | — | Destination tag required for deposits. |
| **Monero** | XMR | — | Private by design; subaddress per deposit. |

## Deposit detection

Deposits are detected by iNCRYPTO's own nodes (public network infrastructure for TON and the XRP Ledger) and credited after the confirmation depth configured for each network. Confirmation depths balance finality against speed and are tuned per network; the current values are shown in the product at deposit time.

## Withdrawals

Withdrawals are signed by iNCRYPTO and broadcast through the same network layer. Every withdrawal passes the account's security controls — second factor and, when enabled, the withdrawal address allow-list — before it is signed. Automated AML screening (iNCRYPTO Shield) is in development.

!!! note "Adding a network"
    New networks are added when we can operate them to the same standard: deterministic deposit detection, a withdrawal path we control end-to-end and, as the target for every network, our own full node.
