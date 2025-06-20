---
title: "Fast, Flexible & Fiercely Efficient Data Access: Envio HyperSync Now Supports Fuel Network"
sidebar_label: "Fast, Flexible & Fiercly Efficient Data Access: Envio HyperSync Now Supports Fuel Network"
slug: /envio-hypersync-powers-data-access-on-fuel-network
---

<img src="/blog-assets/envio-partner-fuel.png" alt="Envio Fuel Partnership Cover Image" width="100%"/>

<!--truncate-->

Come on baby light my fire! 🔥

We’re thrilled to announce that Envio has recently fully integrated its Hypersync service on [Fuel](https://fuel.network/) Network, the Rollup Operating System purpose-built for [Ethereum](https://ethereum.org/en/).

[Envio](https://envio.dev/) is now the go-to solution on Fuel Network for efficient access to real-time and historical data on Fuel. Developers can sync large data sets within seconds! ⚡

## What Envio Supports on Fuel?

[Envio HyperSync’s](https://docs.envio.dev/docs/HyperIndex/overview-hypersync) hyper-performant data infrastructure serves as an accelerated data query layer on top of the Fuel Network that allows application developers and data analysts to easily parse, query, and analyse Fuel data.

With its flexible API, developers and data analysts can interact with the Hypersync API using either [JavaScript](https://www.javascript.com/), [Python](https://www.python.org/) or [Rust](https://www.rust-lang.org/) clients and can choose to query their data in JSON, Arrow, and Parquet data formats.

With support for real-time data analysis and the ability to extract large volumes of historical data within seconds, Hypersync is a perfect solution for building dApps, block explorers, wallets, analytics, and any other data-related activities on Fuel Network.

[Spark Finance](https://sprk.fi/), the world's fastest on-chain order book built on Fuel VM, is a great case study for utilising Hypersync to present near-instant access to order book information to their traders.

<img src="/blog-assets/envio-partner-fuel-1.png" alt="Envio Fuel Partnership Cover Image" width="100%"/>

Using Envio’s HyperSync, application developers do not need to worry about RPC URLs, rate-limiting, or managing infrastructure. Developers can easily sync large datasets in a few minutes, something that would usually take hours or days via RPC.

Learn more [here](https://x.com/Sprkfi/status/1777730945853907128).

## HyperSync on Fuel

_⭐ Hypersync supports Fuel's beta-5 network and will support any future public testnets and Fuel mainnet._

HyperSync is a real-time indexed layer of the Fuel Network and is exposed as a low-level API for developers and data analysts to create niche, flexible, high-speed queries for all on-chain data. Using Envio’s HyperSync, application developers can easily sync large datasets in a few minutes, something that would usually take hours via standard Fuel node GraphQL queries without worrying about managing infrastructure (e.g. hosting archive nodes) or being rate-limited on a public node.

Fuel Developers can interact with the HyperSync API using the JavaScript API (format shown below) and query for specific data with incredible speed.  Some examples of data you can retrieve with HyperSync queries: all transactions from an address, all logs and receipts from a contract, transactions of an asset, or outputs generated by a predicate.

A Rust and Python client for Hypersync will be released soon.

```json
{

// The block to start the query from

"from_block": Number,

// The block to end the query at. If not specified, the query will go until the

//  end of data. Exclusive, the returned range will be [from_block..to_block).

//

// The query will return before it reaches this target block if it hits the time limit

//  configured on the server. The user should continue their query by putting the

//  next_block field in the response into from_block field of their next query. This implements

//  pagination.

"to_block": Number, // Optional, defaults to latest block

/// List of receipt selections, the query will return receipts that match any of these selections and

///  it will return receipts that are related to the returned objects.

"receipts": [{ReceiptSelection}], // Optional

/// List of input selections, the query will return inputs that match any of these selections and

///  it will return inputs that are related to the returned objects.

"inputs": [{InputSelection}], // Optional

/// List of output selections, the query will return outputs that match any of these selections and

///  it will return outputs that are related to the returned objects.

"outputs": [{OutputSelection}], // Optional

// Weather to include all blocks regardless of if they are related to a returned transaction or log Normally

//  the server will return only the blocks that are related to the transaction or logs in the response. But if this

//  is set to true, the server will return data for all blocks in the requested range [from_block, to_block).

"include_all_blocks": bool, // Optional, defaults to false

// The user selects which fields they want returned. Requesting less fields will improve

//  query execution time and reduce the payload size so the user should always use a minimal number of fields.

"field_selection": {FieldSelection},

// Maximum number of blocks that should be returned, the server might return more blocks than this number but

//  it won't overshoot by too much.

"max_num_blocks": Number, // Optional, defaults to no maximum

// Maximum number of transactions that should be returned, the server might return more transactions than this number but

//  it won't overshoot by too much.

"max_num_transactions": Number, // Optional, defaults to no maximum

}
```

For more information and examples, visit the Fuel’s HyperSync documentation [here](https://github.com/enviodev/hypersync-fuel-docs).

## What’s Next?

Envio is a purpose-built, modern blockchain indexing solution and data provider that natively supports indexing any EVM blockchain including [Polygon](https://docs.polygon.technology/tools/data/envio/), [Linea](https://docs.linea.build/build-on-linea/tooling/data-indexers/envio), [Arbitrum](https://docs.arbitrum.io/for-devs/third-party-docs/Envio/#envio-examples), [Base](https://docs.base.org/docs/tools/data-indexers/#envio), [Metis](https://docs.metis.io/dev/tools/indexers/envio#envio-hypersync), and many more. Envio has recently extended support for its hyper-performant data infrastructure to the Fuel VM.

As part of the next evolution in the Envio x Fuel partnership, Envio will be looking to add support for its HyperIndex product to the Fuel ecosystem, a graph-like indexer that equips developers with the necessary tools to easily create custom [GraphQL](https://graphql.org/) APIs and Web3 backends for their applications.

[HyperIndex](https://docs.envio.dev/docs/HyperIndex/overview) is a developer-first, feature-rich data indexing framework that allows indexed data to be easily accessed through GraphQL queries, empowering developers with the ability to retrieve specific information.

HyperIndex is currently only available on EVM networks and offers application developers automatic code generation, flexible language support, quickstart templates, and a reliable cost-effective hosted service, overcoming challenges often associated with managing your own infrastructure.

Here are some HyperIndex features Fuel developers can expect:

- [HyperSync](https://docs.envio.dev/docs/hypersync): To ensure blazing-fast retrieval of historical on-chain data and a seamless developer experience, Envio’s HyperSync automatically powers HyperIndex for 100 x sync times than standard RPC (use of RPC is optional).
- [No-code Quickstart](https://docs.envio.dev/docs/HyperIndex/contract-import): Autogenerate the key boilerplate for an entire Indexer project off single or multiple smart contracts. Deploy within minutes.
- [Multi-chain Support](https://docs.envio.dev/docs/multichain-indexing): Aggregate data across multiple networks into a single database. Query all your data with a unified GraphQL API.
- [Asynchronous Mode](https://docs.envio.dev/docs/async-mode): Fetch data from off-chain storage such as IPFS, or contract state (e.g. smart contract view functions).
- [Factory Contracts](https://docs.envio.dev/docs/dynamic-contracts): Automatically process events emitted by all child contracts that are created by the specified factory.
- [Hosted Service](https://docs.envio.dev/docs/hosted-service): A managed service platform for building, hosting and querying Envio's Indexers with guaranteed uptime and performance service level agreements.

## Relevant Links

- [Envio HyperSync](https://docs.envio.dev/docs/HyperIndex/overview-hypersync)
- [Fuel’s HyperSync Documentation](https://github.com/enviodev/hypersync-fuel-docs)

## About Fuel

[Fuel](https://fuel.network/) is an operating system purpose-built for Ethereum rollups. Fuel's unique architecture allows rollups to solve for PSI (parallelization, state minimized execution, interoperability). Powered by the FuelVM, Fuel aims to expand Ethereum's capability set without compromising security or decentralization.

[Website](https://fuel.network/) | [X](https://twitter.com/fuel_network?lang=en) | [Discord](https://discord.com/invite/xfpK4Pe)

## About Envio

[Envio](https://envio.dev/) is a dev-friendly, speed-optimized, modern blockchain indexing solution that addresses the limitations of traditional blockchain indexing approaches and gives developers peace of mind. By harnessing the power of Envio, developers can overcome the challenges posed by latency, reliability, and costs across various sources. Envio is the front door for any application’s need to access, transform, and save real-time or historical data, from any EVM-compatible smart contracts. If you're a blockchain developer looking to enhance your development process and unlock the true potential of Web3 infrastructure, look no further.

Join our growing community of Web3 developers, check out our docs, and let's work together to revolutionize the blockchain world and propel your project to the next level.

[Website](https://envio.dev/) | [X](https://twitter.com/envio_indexer) | [Discord](https://discord.com/invite/gt7yEUZKeB) | [Hey](https://hey.xyz/u/envio) | [Medium](https://medium.com/@Envio_Indexer) | [YouTube](https://www.youtube.com/channel/UCR7nZ2yzEtc5SZNM0dhrkhA) | [Reddit](https://www.reddit.com/user/Envio_indexer)
