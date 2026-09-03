---
title: Integrations
---

# Integrations <span class="inc-status inc-status--dev">Preview</span>

The public API is not yet released. This section describes the integration model so partners can plan ahead; endpoint references, SDKs and sandbox access will be published with the API release.

## Merchant acquiring (iNCRYPTO Pay)

A merchant integration follows a familiar shape:

1. **Create an invoice** for an amount in a fiat or crypto denomination. iNCRYPTO returns a hosted checkout URL and a payment address for the asset the customer selects.
2. **Customer pays** on-chain. Detection is performed by iNCRYPTO's own nodes.
3. **Webhook** notifies the merchant's backend as the payment progresses: seen, confirmed, settled, or expired.
4. **Settlement** to the merchant's balance in the asset of their choice, with the exchange leg handled by iNCRYPTO Exchange when the customer paid in a different asset.

Every step is screened by iNCRYPTO Shield; a flagged payment is held rather than settled, and the merchant is informed through the same webhook channel.

## Webhooks

Webhooks are signed. Each delivery carries a timestamp and a signature over the payload computed with a per-endpoint secret, so a merchant can verify authenticity and reject replays. Deliveries are retried with backoff until acknowledged.

## Rate feeds for aggregators

iNCRYPTO publishes exchange directions and rates in the format used by rate aggregators. The feed specification — fields, update frequency and the meaning of reserve figures — will be published on this page.

## Authentication

Partner access uses API keys scoped to a merchant account, with request signing and optional IP allow-listing. Keys are managed from the dashboard.

## Get in touch

If you are planning an integration, write to [hello@incrypto.me](mailto:hello@incrypto.me) — early partners get access to the sandbox before the public release.
