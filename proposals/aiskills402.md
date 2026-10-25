# AISkills402

## Basic details
- Project name: AISkills402
- What does it do? (2–3 sentences): A store of tested AI agent skill files (SKILL.md, Agent Skills format). An agent searches the catalog for free and buys the file of one skill once over x402, for cents in USDC on Base; re-downloads and new versions of a bought skill are free. Each skill card says how the skill was tested on a strong and a weak model, with and without the skill.
- Type: API (plus a free remote MCP server for search)
- Official website: https://aiskills402.com
- Logo URL: https://aiskills402.com/apple-icon.png
- Documentation or getting-started link: https://aiskills402.com/llms.txt (OpenAPI: https://api.aiskills402.com/openapi.json; MCP: https://mcp.aiskills402.com/mcp)
- Public support channel: hello@aiskills402.com (the contact published on the site and in /.well-known/ai-plugin.json)

## Networks and activity
- Networks: Base
- Public explorer or analytics link, if available: https://basescan.org/address/0x8e37022edcf0f21cf3c9f93fee9d4d32519f36f4 (the receiving address; the same operator's 402registry.com, 402cron.com and 402post.com receive on it too)
- App contract/program or receiving addresses, with their networks, if available: Base (eip155:8453) payee 0x8e37022edcf0f21cf3c9f93fee9d4d32519f36f4
- Proof that you represent the project: see "Ownership reference" below.

## Payments — only if your product accepts payments
- Paid endpoint and HTTP method: GET https://api.aiskills402.com/v1/skills/{slug}/file — a one-time purchase of one skill file. The price is on each skill card and in the 402 (from $0.01; for example cold-email is $0.03, 30000 atomic). Also GET /v1/packs/file?skills=… (10 or more skills in one payment, discounted). Free: the catalog, skill cards, MCP search, and re-download with the purchase token.
- Facilitator used: Coinbase CDP (https://api.cdp.coinbase.com/platform/v2/x402)
- Payment scheme/version: x402 v2, exact (USDC transferWithAuthorization; extra name "USD Coin", version "2")
- Token contract/mint and decimals: USDC on Base, 0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913, 6 decimals
- Successful payment transaction link for each supported network: see "Payment example" below.
- Facilitator applicants: Not applicable

## Website application
- Website application reference, if you have one: none
- Related issue or previous pull request, if any: none. The same operator's 402registry, 402cron and 402post (same payee) are proposed in separate pull requests.

## Payment example (Base mainnet, paid by an outside wallet)
- Request: GET https://api.aiskills402.com/v1/skills/cold-email/file (one skill file)
- Amount: 0.03 USDC (30000 atomic, 6 decimals) on Base mainnet (eip155:8453), 2026-10-01 12:01 UTC
- Payer: 0xc9c7b38c0942914fc8ea12063bc92dcd3b581670 — not a wallet of the operator
- Transaction: https://basescan.org/tx/0x72d2dfe803256939db9ad2d5b89ced1a1afb79c527b4b02fb01b7fe3f304927d (block 52033362, status success; USDC Transfer 0xc9c7…1670 → 0x8e37…36f4, 0.03 USDC; submitted by the facilitator's relayer 0xb87e1a2cc2b4643f2892768e80e41167f17c5860)
- The operator's own test purchases come only from 0xa340966d806f114483d671f6bf934daebbdff8dc (stated in llms.txt, "Verify before paying") and are not used as evidence here.

## Ownership reference
- https://aiskills402.com/llms.txt, section "Contact": the operator Georgi Kalchev, and the line "Operator on GitHub: https://github.com/paranormalen2" — the account that opened this pull request.
- The listing repository https://github.com/paranormalen2/aiskills402-mcp is in the same account; the Official MCP Registry entry com.aiskills402/mcp is published under the domain-verified namespace.

## Buyer guide
- Exact x402 v2 flow (402 PAYMENT-REQUIRED → PAYMENT-SIGNATURE → PAYMENT-RESPONSE receipt), what is charged when settlement fails or is uncertain, and what to verify before signing: https://aiskills402.com/llms.txt, sections "How to buy (HTTP)", "What you are charged" and "Verify before paying"; https://aiskills402.com/trust.
