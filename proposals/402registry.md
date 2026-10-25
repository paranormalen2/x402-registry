# 402registry

## Basic details
- Project name: 402registry
- What does it do? (2–3 sentences): Checks whether AI agents and AI crawlers can actually see a website: one plain HTTP fetch with no JavaScript, the way GPTBot, ClaudeBot, PerplexityBot and OAI-SearchBot fetch pages. Every finding quotes what the fetch returned, with a fix. A passing check earns a dated badge and a free listing in a public catalog.
- Type: API (plus a remote MCP server)
- Official website: https://402registry.com
- Logo URL: https://402registry.com/favicon.png
- Documentation or getting-started link: https://402registry.com/llms.txt (OpenAPI: https://402registry.com/openapi.json; MCP: https://402registry.com/mcp)
- Public support channel: abuse@402registry.com (the contact published in the terms and in /.well-known/ai-plugin.json)

## Networks and activity
- Networks: Base
- Public explorer or analytics link, if available: https://basescan.org/address/0x8e37022edcf0f21cf3c9f93fee9d4d32519f36f4 (the receiving address; the same operator's aiskills402.com, 402cron.com and 402post.com receive on it too)
- App contract/program or receiving addresses, with their networks, if available: Base (eip155:8453) payee 0x8e37022edcf0f21cf3c9f93fee9d4d32519f36f4
- Proof that you represent the project: see "Ownership reference" below.

## Payments — only if your product accepts payments
- Paid endpoint and HTTP method: GET https://402registry.com/buy/one?site=<https URL> — one check, $0.01 (10000 atomic). Also GET /buy/catalog — the catalog snapshot as one JSON file, $0.005. Free: GET /api/check?url= (the last dated verdict) and /registry.json.
- Facilitator used: Coinbase CDP (https://api.cdp.coinbase.com/platform/v2/x402)
- Payment scheme/version: x402 v2, exact (USDC transferWithAuthorization; extra name "USD Coin", version "2")
- Token contract/mint and decimals: USDC on Base, 0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913, 6 decimals
- Successful payment transaction link for each supported network: see "Payment example" below.
- Facilitator applicants: Not applicable

## Website application
- Website application reference, if you have one: none
- Related issue or previous pull request, if any: none. The same operator's AISkills402, 402cron and 402post (same payee) are proposed in separate pull requests.

## Payment example (Base mainnet, paid by an outside wallet)
- Request: GET https://402registry.com/buy/one?site=… (one check)
- Amount: 0.01 USDC (10000 atomic, 6 decimals) on Base mainnet (eip155:8453), 2026-10-19 15:52 UTC
- Payer: 0x171d8021b98c53dcbb3c9c30cbbbeb1b01850fca — not a wallet of the operator
- Transaction: https://basescan.org/tx/0x05a197195a5e38a9450e0493239a2b309fd90fa0ca89a7bc8e0b76203dd0e2f5 (block 52817904, status success; USDC Transfer 0x171d…0fca → 0x8e37…36f4, 0.01 USDC; submitted by the facilitator's relayer 0x64cc42b1ce598e3abcfbb64df4688521ddbf1f0a)

## Ownership reference
- https://402registry.com/llms.txt, section "Operator": Georgi Kalchev and "GitHub: https://github.com/paranormalen2" — the account that opened this pull request.
- The listing repository https://github.com/paranormalen2/402registry-mcp is in the same account; the Official MCP Registry entry com.402registry/402registry is published under the domain-verified namespace.

## Buyer guide
- Products, prices, the exact x402 v2 payment requirements and what is charged: https://402registry.com/llms.txt, section "Buy a check (x402)"; https://402registry.com/trust (how to check the 402 terms and the receiving wallet before paying).
