---
title: iNTRADE
---

# iNTRADE <span class="inc-status inc-status--dev">In development</span>

**Systematic, risk-first investment portfolios on perpetual futures.** iNTRADE runs a multi-strategy portfolio on USDT-margined perpetual futures and manages it against a risk budget you choose. It will be available at [trade.incrypto.me](https://trade.incrypto.me).

## What it is

- **A portfolio, not a bot.** Several independent, rules-based strategies with different mechanics and holding horizons, combined so that their drawdowns do not coincide: a trend-following core and components that earn in the regimes where trend does not.
- **You choose a risk tier, not leverage.** Every position is sized from a target volatility and a drawdown budget. Leverage is a derived quantity, capped per tier, never an input.
- **Fully systematic.** No discretionary trading. Every sizing decision, every cut and every stop is written to a decision journal with its reason, so any position is explainable after the fact.

## Risk tiers

| Tier | Target volatility | Drawdown budget | Margin mode |
|---|---|---|---|
| **minimal** | ~8 % a year | ~10 % | isolated |
| **medium** | ~15 % a year | ~20 % | cross |
| **maximum** | ~25 % a year | ~35 % | cross |

Figures are indicative. They are calibrated during validation and only ever tightened, never loosened.

## How risk is controlled

The strategy layer produces a direction and a strength. Money enters only in the portfolio layer, and every step below can only reduce exposure — a strategy cannot breach a tier limit from the inside.

| Control | What it does |
|---|---|
| **Volatility targeting** | Positions scale inversely with realised volatility so the portfolio stays at the tier's target. |
| **Drawdown ladder** | As drawdown approaches the budget, exposure is cut in steps. At the budget everything is closed and trading stops. The stop persists across restarts and is released only by a human. |
| **Loss limits** | Daily and weekly limits block new entries; loss streaks trigger a pause. |
| **Correlation regime** | If strategies start moving together, gross exposure is halved. |
| **Liquidation distance** | Monitored continuously; positions are reduced long before the exchange would act. |
| **Exchange reconciliation** | Positions, orders and balances are reconciled against the venue, which is the source of truth. |
| **Execution** | Maker-first, post-only orders; protective stops on mark price. |

## Custody

| | Non-custodial (first) | Pooled (later) |
|---|---|---|
| Where funds sit | Your own sub-account on a leading derivatives venue | Pooled accounts operated by iNCRYPTO, one per tier |
| What iNTRADE holds | A **trade-only API key** — no withdrawal permission, ever | Full control of the pooled account |
| Accounting | Your account equity | Units and NAV, daily cut-off |
| Lock-up | None — orderly exit: entries stop, positions close, you withdraw | None — withdrawals at the next NAV cut-off |
| Requirements | A funded sub-account | KYC/AML before the first deposit |

## Instruments

BTC and ETH perpetuals at launch. Further instruments are added only after they pass the same validation.

## Path to launch

Nothing described here has traded real funds yet. Launch follows a gated protocol, and no gate is relaxed to make a stage pass:

1. **Backtest** — multi-year history including several stress episodes, walk-forward with out-of-sample periods, overfitting-aware statistics, cost and funding modelled explicitly.
2. **Paper trading** — a minimum of eight weeks on the venue's demo environment, compared against the backtest.
3. **Live smoke** — small real capital to verify execution end to end.
4. **Beta** — limited capital on the minimal tier under observation.
5. **Client accounts** — non-custodial model opens.
6. **Pools** — pooled accounts by tier, after legal and compliance review.

A strategy that fails its gate is removed from the portfolio, not tuned until it passes.

## What we do not publish

Signal definitions, parameters, allocation rules and the research behind them are proprietary. What we do publish is everything that governs your risk: tiers, limits, custody model and validation status. Expected return figures are not published until they are confirmed by backtest and paper trading.

!!! warning "Not investment advice"
    Trading perpetual futures involves substantial risk of loss, including loss of the full drawdown budget of your tier. iNTRADE is a software product with a defined risk model; it is not a guarantee of return. Backtested or simulated performance is not indicative of future results. Nothing on this page is investment advice.

Early-access enquiries: [hello@incrypto.me](mailto:hello@incrypto.me).
