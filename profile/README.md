# GraphOps

GraphOps builds and operates onchain data systems. Use GraphOps RPC, Subgraphs, and Substreams to
read chain state, query indexed entities, and stream ordered blocks without running data
infrastructure.

[Docs](https://docs.graphops.xyz) · [Create account](https://platform.graphops.xyz/auth/register) · [Pricing](https://graphops.xyz/pricing/) · [Website](https://graphops.xyz)

## Get started

1. [Create an account](https://platform.graphops.xyz/auth/register) and create or join an organization.
2. [Create an API key](https://platform.graphops.xyz/organizations/current/api-keys) for the service you plan to use. Copy it when it is shown; it is not shown again.
3. Send your first request:

```sh
curl --fail-with-body --silent --show-error "https://rpc.graphops.xyz/v1/evm/1" \
  -H "Authorization: Bearer ${GRAPHOPS_API_KEY}" \
  -H "Content-Type: application/json" \
  --data '{"jsonrpc":"2.0","id":1,"method":"eth_blockNumber","params":[]}'
```

Not sure which service fits? [Choose a data service](https://docs.graphops.xyz/choose-a-service).

## Data services

| Service | Use it for | Endpoint | Start here |
| --- | --- | --- | --- |
| **RPC** | Read chain state, submit transactions, and subscribe to new blocks and logs on EVM and Bitcoin networks. | `https://rpc.graphops.xyz/v1/evm/<CHAIN_ID>` (JSON-RPC, WebSocket) | [Quickstart](https://docs.graphops.xyz/rpc/getting-started) · [Networks](https://docs.graphops.xyz/rpc/networks) · [Methods](https://docs.graphops.xyz/rpc/methods) · [API](https://docs.graphops.xyz/rpc/api) |
| **Subgraphs** | Query indexed entities over GraphQL from a public Subgraph, or deploy and release your own. | `https://subgraphs.graphops.xyz/v1/...` (GraphQL) | [Quickstart](https://docs.graphops.xyz/subgraphs/getting-started) · [Networks](https://docs.graphops.xyz/subgraphs/networks) · [Deploy with Graph CLI](https://docs.graphops.xyz/subgraphs/guides/deploy-with-graph-cli) · [API](https://docs.graphops.xyz/subgraphs/api) |
| **Substreams** | Backfill and stream ordered block data into your own database or processor with the standard Substreams CLI. | `https://<CHAIN_ID>.evm.substreams.graphops.xyz` (gRPC) | [Quickstart](https://docs.graphops.xyz/substreams/getting-started) · [Networks](https://docs.graphops.xyz/substreams/networks) · [Run a sink](https://docs.graphops.xyz/substreams/guides/run-a-sink) · [API](https://docs.graphops.xyz/substreams/api) |

All three services use organization API keys and draw from one credit balance. See
[Billing and credits](https://docs.graphops.xyz/platform/billing-and-credits) and
[Usage and limits](https://docs.graphops.xyz/platform/usage-and-limits).

## Build for production

- [Production readiness](https://docs.graphops.xyz/production-readiness): credentials, consistency, limits, retries, observability, and recovery.
- [API keys](https://docs.graphops.xyz/platform/api-keys): separate keys per environment, rotation, and revocation.
- [Endpoint Aliases](https://docs.graphops.xyz/subgraphs/guides/manage-aliases): keep a stable Subgraph URL while you release new versions.
- [Consistency and finality](https://docs.graphops.xyz/rpc/concepts/consistency-and-finality) and [Cursors and reorgs](https://docs.graphops.xyz/substreams/concepts/cursors-and-reorgs): handle reorgs safely.
- [Team and roles](https://docs.graphops.xyz/platform/team-and-roles): invite teammates and control access.

## For AI agents and LLM tools

[docs.graphops.xyz/llms.txt](https://docs.graphops.xyz/llms.txt) indexes every docs page in
Markdown, and [llms-full.txt](https://docs.graphops.xyz/llms-full.txt) has the complete
documentation.

## About

GraphOps runs these services in production and contributes to the indexing systems of
[The Graph](https://thegraph.com/) as a [core developer](https://thegraph.com/blog/graphops-core-dev/).
Read more on the [company page](https://graphops.xyz/company/).

Questions? Ask in the platform chat, email [hello@graphops.xyz](mailto:hello@graphops.xyz), or
[talk to the team](https://graphops.xyz/contact/). Follow [@graphopsxyz](https://x.com/graphopsxyz).
