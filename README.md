# x402 Discovery Index

A live directory of 12,000+ x402-enabled APIs, built for autonomous agents 
that discover and pay for services programmatically using the 
x402 protocol (https://x402.org).

## What Is This?

The x402 protocol lets HTTP APIs charge per-request using on-chain payments 
on Base (Ethereum L2). The x402 Discovery Index aggregates these APIs into 
one searchable layer — so agents don't need to know every endpoint in advance.

## How Agents Use It

Send a POST request to search the index:

POST http://187.77.201.36:9402/v1/search
Content-Type: application/json

{
  "query": "llm inference",
  "filters": {
    "network": "eip155:8453",
    "scheme": "exact"
  },
  "page": { "limit": 20, "offset": 0 },
  "mode": "agent"
}

The API uses x402 for payment — your agent pays 1000 USDC units per search 
request directly on Base. No API keys, no subscriptions.

Full tutorial: http://187.77.201.36:9402/tutorial

## Currently Indexed

| Provider | Category | Endpoints |
|----------|----------|-----------|
| CoinGecko | Crypto market data | 22 |
| CDP x402 Bazaar | Mixed | 12,000+ |

Updated automatically as new providers are verified and listed.

## List Your x402 API

If you run an x402-enabled API and want it discovered by agents:

- One-time listing fee — no subscription
- Your endpoint appears in search results immediately after verification
- Agents querying this index pay you directly via x402

To list your API, open an issue in this repo with:
1. Your endpoint URL
2. Your x402 payment address
3. Brief description of what your API does

We will verify and list within 24 hours.

## Contact

Questions? Open an issue in this repo.

- [fitze-x402-tools](https://fitze-x402-seller.app.workbuddy.host) — 13 pay-per-call x402 tools on Base USDC ($0.005-$0.01/call, no API key): web_fetch, domain_intel, github_repo, token_intel, repo_diligence, web_brief, stock_quote, free_url_check, usgs_earthquakes, open_meteo_weather, exchange_rates, sec_edgar_search, fda_recalls. Agent-payable via x402; MCP at `/mcp`; discovery at `/.well-known/x402`; payout to `0x0751...` on Base. ([MCP](https://fitze-x402-seller.app.workbuddy.host/mcp) | [Discovery](https://fitze-x402-seller.app.workbuddy.host/.well-known/x402))