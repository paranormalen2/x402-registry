# 402cron

## Basic details
- Project name: 402cron
- What does it do? (2–3 sentences): Paid cron for AI agents. An agent registers a public HTTPS URL and a cron schedule, and the service calls it on time with a signed request, billing one prepaid delivery per attempt. Deliveries are bought in packs over x402; there is no account and no API key — the paying wallet is the identity.
- Type: API (plus a remote MCP server)
- Official website: https://402cron.com
- Logo URL: https://402cron.com/og.png
- Documentation or getting-started link: https://402cron.com/llms.txt (OpenAPI: https://402cron.com/openapi.json; MCP: https://402cron.com/mcp)
- Public support channel: abuse@402cron.com (the contact published in the terms and in /.well-known/ai-plugin.json)

## Networks and activity
- Networks: Base
- Public explorer or analytics link, if available: https://basescan.org/address/0x8e37022edcf0f21cf3c9f93fee9d4d32519f36f4 (the receiving address; the same operator's aiskills402.com, 402registry.com and 402post.com receive on it too)
- App contract/program or receiving addresses, with their networks, if available: Base (eip155:8453) payee 0x8e37022edcf0f21cf3c9f93fee9d4d32519f36f4
- Proof that you represent the project: see "Ownership reference" below.

## Payments — only if your product accepts payments
- Paid endpoint and HTTP method: GET https://402cron.com/buy/{pack} — a prepaid pack of deliveries: trial, 20 deliveries for $0.02 (20000 atomic); starter, 2,000 for $1; month, 50,000 for $25. Packs never expire. Free: pricing, docs and /health.
- Facilitator used: Coinbase CDP (https://api.cdp.coinbase.com/platform/v2/x402)
- Payment scheme/version: x402 v2, exact (USDC transferWithAuthorization; extra name "USD Coin", version "2")
- Token contract/mint and decimals: USDC on Base, 0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913, 6 decimals
- Successful payment transaction link for each supported network: see "Payment example" below.
- Facilitator applicants: Not applicable

## Website application
- Website application reference, if you have one: none
- Related issue or previous pull request, if any: none. The same operator's AISkills402, 402registry and 402post (same payee) are proposed in separate pull requests.

## Payment example (Base mainnet, paid by an outside wallet)
- Request: GET https://402cron.com/buy/trial (20 deliveries)
- Amount: 0.02 USDC (20000 atomic, 6 decimals) on Base mainnet (eip155:8453), 2026-10-23 23:35 UTC
- Payer: 0x7722dfae6bbed2fd02dc07455c2f5bf14be25e4a — not a wallet of the operator
- Transaction: https://basescan.org/tx/0xc15f5bb0ca40200d6a8d5f0595b01af0b323b2430269a70585521a08d50ae28a (block 53004600, status success; USDC Transfer 0x7722…5e4a → 0x8e37…36f4, 0.02 USDC; submitted by the facilitator's relayer 0x59b7ebc67a3d627fabaf06768c818638452ae704)

## Ownership reference
- https://402cron.com/llms.txt, section "Operator": Georgi Kalchev and "GitHub: https://github.com/paranormalen2" — the account that opened this pull request.
- The listing repository https://github.com/paranormalen2/402cron-mcp is in the same account; docs and examples: https://github.com/402cron/402cron (linked from the same llms.txt section). The Official MCP Registry entry com.402cron/402cron is published under the domain-verified namespace.

## Buyer guide
- Packs, prices, how to buy and what a delivery costs: https://402cron.com/llms.txt, sections "Packs" and "What you need"; https://402cron.com/docs (how to buy, register a task and read a delivery).
