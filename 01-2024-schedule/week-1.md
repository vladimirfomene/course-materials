---
description: Building on bitcoin and setting up a bitcoin development environment
---

# Week 1

## Prerequisites
We would like you to download some source code and attempt to compile it by following its build instructions before the course begins. This is to prevent any delays when starting on the day.

Please download/clone the following tools/repositories and try to follow and complete their build processes:

| Software       | Repository                                                                                   |
| -------------- | -------------------------------------------------------------------------------------------- |
| TABconf wallet | [https://github.com/KayBeSee/tabconf-workshop](https://github.com/KayBeSee/tabconf-workshop) |
| Bitcoin Core   | [https://github.com/bitcoin/bitcoin](https://github.com/bitcoin/bitcoin)                     |
| LND            | [https://github.com/lightningnetwork/lnd](https://github.com/lightningnetwork/lnd)           |
| Polar          | [https://lightningpolar.com/](https://lightningpolar.com)                                    |

{% hint style="warning" %}
Don't run `bitcoind` without specifying `regtest` (or `signet`) as the network in the configuration file (`bitcoin.conf`) or as a command line argument (see `bitcoind --help`). Otherwise you will start synchronising blocks for mainnet which is over 400 GB! At this point, you don't even need to run bitcoind just yet.
{% endhint %}


## Goals

* Discuss and understand bitcoin philosophy
* Become comfortable and proficient in setting up bitcoin developer environments
* Be able to run and interface with Bitcoin Core and LND
  * Understand signet and regtest
  * Connect Bitcoin Core and LND programmatically
  * Interface with Bitcoin Core and LND using the CLI tools
  * Programmatic control of bitcoind and LND
  * Comfortable with running the full test suite(s) of Bitcoin Core
* Build a toy bitcoin wallet using a library
  * Add additional functionality of your choosing
* Develop a robust understanding of bitcoin topics both in theory and in practice:
  * Random number generation
  * Keys and key material
  * Derivation paths
  * Address types
  * Coin selection
  * The differences between keys, address and digital signatures
* Gain experience with developing and using a Bitcoin wallet UI
* Introduction to Technical Writing 
  * Learn the critical basics of technical writing
  * Develop skills for making documentation more accessible to all.


## Monday & Tuesday

1. Introduction to Btrust Builders Programme
2. Programme structure
3. Icebreakers
4. Bitcoin Philosophy
5. Why we bitcoin

## Wednesday

### Resources

| Name                                                               | Link                                                                                                                                                                                                   |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Setting Up Bitcoin Core and Lightning On Windows using WSL | [https://tobiojuolape.hashnode.dev/preview/63ca548a415abc00080231c5](https://tobiojuolape.hashnode.dev/preview/63ca548a415abc00080231c5)|
| Setting Up a Bitcoin and Lightning Daemon on Mac from source | [https://dev.to/timothy_masiko/setting-up-a-bitcoin-and-lightning-network-daemon-on-mac-from-source-17hb](https://dev.to/timothy_masiko/setting-up-a-bitcoin-and-lightning-network-daemon-on-mac-from-source-17hb)|
| Lightning Book - Bitcoin Fundamentals review                       | [https://lnbook.256k1.dev/#bitcoin\_fundamentals\_review](https://lnbook.256k1.dev/#bitcoin\_fundamentals\_review)                                                                                     |
| BIP0032                                                            | [https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)                                                                       |
| Learn Bitcoin From The Command Line | [https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line)|
| Bitstein - Setting up a bitcoin lightning network test environment | [https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a) |
| Why Bitcoin Addreess is not like an account number | [https://sadeeqcode.medium.com/why-bitcoin-address-is-not-like-an-account-number-e5a5261a0605](https://sadeeqcode.medium.com/why-bitcoin-address-is-not-like-an-account-number-e5a5261a0605)|

### Exercises
1. Read about Hierarchical Deterministic Wallets in BIP0032.
   * You do not need to read/understand the child key derivation functions.
   * You should conclude with a strong understanding of how parent and child keys are derived from each other, and from a master seed .
2. Learn Bitcoin From The Command Line: [Using the bitcoin CLI](https://github.com/BlockchainCommons/Learning-Bitcoin-from-the-Command-Line/blob/master/03_0_Understanding_Your_Bitcoin_Setup.md).
You are expected to:
    1. Become comfortable working with the bitcoin-cli command-line interface
    2. Create an Address to Receive Bitcoin Funds
    3. Use Basic Wallet Commands
    4. Create an Address to Receive Bitcoin Funds
3. Set up a manual bitcoin and lightning developer environment on regtest by following the guide from Bitstein: [Setting up a Bitcoin/Lightning test environment](https://medium.com/@bitstein/setting-up-a-bitcoin-lightning-network-test-environment-ab967167594a)
   * Note, this environment should ideally be built using Bitcoin Core and LND which have been build from source by yourself.
4. Run all Bitcoin Core unit tests
5. Choose area of the codebase you're interested in, pick a functional test that covers it, and then run that test
   * hint: see documentation in `test/README.md` for clues on how to run individual tests)

### Deliverables

1. Take a screenshot of the address you created using the cli, send testnet funds to that address using this [faucet](https://bitcoinfaucet.uo1.net/) and share the screenshot of the transaction on the testnet [explorer](https://mempool.space/testnet) and its balance
2. Screenshot of your lightning developer environment resulting from the guide from Bitstein.

### Thursday

### Resources

| Name                                                               | Link                                                                                                                                                                                                   |
| ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| TABConf 2021 Building Your own bitcoin wallet with BitcoinJS       | [https://youtu.be/Bwz2P2hPVpk](https://youtu.be/Bwz2P2hPVpk)                                                                                                                                           |
| Create Keys, wallets, addresses and Build a Bitcoin Transaction | [https://medium.com/@bitcoindeezy/bitcoin-basics-programming-with-bitcoinjs-lib-4a69218c0431](https://medium.com/@bitcoindeezy/bitcoin-basics-programming-with-bitcoinjs-lib-4a69218c0431)|



### Exercise

2. Build a Bitcoin wallet and make a bitcoin transaction following this programming guide [here](https://medium.com/@bitcoindeezy/bitcoin-basics-programming-with-bitcoinjs-lib-4a69218c0431). 
    1. Note that the bitcoin library does not neccesarily have to be bitcoinjs-lib, any bitcoin library in the programming language of your choice can achieve the same results
    2. You can add an address functionality that allows you to generate one or more different address types e.g. P2PK, P2PKH, P2SH, P2WPKH, P2WSH, P2TR, for the user to choose from


### Deliverables
1. TABConf: please send us file: `src/util/bitcoinjs-lib.ts`.
2. Take a screenshot of the address you created, the transaction on the testnet faucet and its balance


### Friday
