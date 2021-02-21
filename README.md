[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/solana-labs/dapp-scaffold)

# 🏗 Solana App Scaffold
Scaffolding for a dapp built on Solana

# Quickstart

```bash
git clone https://github.com/solana-labs/dapp-scaffold.git

cd dapp-scaffold
```

```bash

npm install

```

```bash

npm start

```

# Environment Setup
1. Install Rust from https://rustup.rs/
2. Install Solana v1.5.0 or later from https://docs.solana.com/cli/install-solana-cli-tools#use-solanas-install-tool
3. Install Node
4. Install NPM

# Build Smart Contract (compiled for BPF)

```bash
$ cargo build-bpf
$ cargo test-bpf
```
# Directory structure

## program

Solana program template in Rust

### src/lib.rs
* process_instruction function is used to run all calls issued to the smart contract

## src/actions

Setup here actions that will interact with Solana programs using sendTransaction function

## src/contexts

React context objects that are used propagate state of accounts across the application

## src/hooks

Generic react hooks to interact with token program:
* useUserBalance - query for balance of any user token by mint, returns:
    - balance
    - balanceLamports
    - balanceInUSD
* useAccountByMint
* useTokenName
* useUserAccounts

## src/views

* home - main page for your app
* faucet - airdrops SOL on Testnet and Devnet