## ProxiRun - Decentralized Compute on Aptos

### Overview 
ProxiRun is a decentralized marketplace for Compute built on Aptos. 
It provides a marketplace to request computations in a distributed way, on a fair and transparent smart contract-based marketplace.
It currently focuses on ML / AI generations (text completion, image generation, voice generation) with plans to expand support to ZK proofs and access to a wider selection of ML models. 

This project was created as a submission for [Code Collision](https://dorahacks.io/hackathon/code-collision/detail), a global Hackathon for the Aptos blockchain.

As part of this submission we created:
- [A smart contract](https://github.com/ProxiRun/contract) for users to submit work requests, and workers to bid on execution. The smart contract implements an auction system in Move.  
- [The main webapp](https://proxirun-web.vercel.app/) to allow users to more easily interact with the protocol, either by submitting new requests for execution or consulting the generated outputs
- [An analytics platform](https://proxirun-analytics.vercel.app/) which uses Nodit as a data provider, showcasing usage on the platform, historical pricing for requests and much more!
- [A Rust SDK](https://github.com/ProxiRun/proxirun/tree/main/proxirun-sdk) containing definitions for events, type definitions and methods to interact with the contract and the auction orchestrator
- [The auction orchestrator](https://github.com/ProxiRun/proxirun/tree/main/orchestrator) updating the smart contract state and managing submissions by workers 
- [A reference worker](https://github.com/ProxiRun/proxirun/tree/main/worker) that waits for new work requests by users, can bid on work request auctions and submit completed work to the orchestrator
- [A Rust-based event listener](https://github.com/ProxiRun/proxirun/tree/main/chain_listener) which listens to events fron the [Transaction Stream Service](https://aptos.dev/en/build/indexer/txn-stream)


