<img align="right" width="120" height="80" src="share/pixmaps/nsis-header.bmp">
<h1 align="center">
<img src="https://raw.githubusercontent.com/litemoney/litemoney/master/share/pixmaps/litemoney256.svg" alt="Litemoney"width="256"/>
<br/><br/>
Litemoney Core  
</h1>

<p align="center">
  <strong>LITEMONEY: Payment Protocol And Decentralized Financial Network.</strong><br>
  Open Source | High-Speed Settlement | Permissionless Infrastructure
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Status-Mainnet--Ready-green" alt="Status">
  <img src="https://img.shields.io/badge/License-MIT-blue" alt="License">
  <img src="https://img.shields.io/badge/Network-Layer--1-orange" alt="Layer-1">
</p>

## What is Litemoney?

**Litemoney (LTM)** is an innovative, decentralized cryptocurrency designed to function as a primary medium of exchange. Litemoney provides a secure, transparent, and immutable ledger for global peer-to-peer transactions.

The mission of Litemoney is to provide a functional alternative to traditional currencies by offering a scalable payment infrastructure that is not controlled by any central authority. 

### Peer-to-Peer Network
Litemoney operates on a distributed network of nodes. Every node maintains a full copy of the blockchain, ensuring that the history of all transactions is transparent and verifiable by anyone, anywhere.

### Transaction Processing & Settlement
Unlike slower legacy systems, Litemoney is engineered for speed. With a **2.5 minute block time**, transactions are confirmed and settled across the network rapidly. This makes it a viable tool for real-world merchant payments and rapid digital transfers.

### Network Security
The network is secured via the **Scrypt Algorithm**. Miners provide computational power to validate transactions and secure the blockchain against double-spending attacks. In exchange for this work, miners receive a block reward, ensuring a fair and decentralized distribution of the currency.

### Difficulty Management
To maintain the stability of the 2.5 Minutes block interval, Litemoney utilizes **DigiShield**. This technology allows the network to adjust mining difficulty in real-time after every block, protecting the network from hashrate fluctuations and ensuring consistent payment processing times.

## Usage

To start your journey with Litemoney Core, see the [installation guide](INSTALL.md) and the [getting started](doc/getting-started.md) tutorial.

The JSON-RPC API provided by Litemoney Core is self-documenting and can be browsed with `litemoney-cli help`, while detailed information for each command can be viewed with `litemoney-cli help <command>`.

### Ports

Litemoney Core by default uses port `7555` for peer-to-peer communication that
is needed to synchronize the "mainnet" blockchain and stay informed of new
transactions and blocks. Additionally, a JSONRPC port can be opened, which
defaults to port `7554` for mainnet nodes. It is strongly recommended to not
expose RPC ports to the public internet.

| Function | mainnet | testnet | regtest |
| :------- | ------: | ------: | ------: |
| P2P      |   7555 |   9422 |   19333 |
| RPC      |   7554 |   9421 |   19332 |

## Ongoing development

Litemoney Core is an open source and community driven software. The development
process is open and publicly visible; anyone can see, discuss and work on the
software.

Main development resources:

* [GitHub Projects](https://github.com/litemoney/litemoney/projects) is used to
  follow planned and in-progress work for upcoming releases.
* [GitHub Discussions](https://github.com/litemoney/litemoney/discussions) is used
  to discuss features, planned and unplanned, related to both the development of
  the Litemoney Core software, the underlying protocols and the LTM asset.

### Branches
There are 4 types of branches in this repository:

- **master:** Unstable, contains the latest code under development.
- **maintenance:** Stable, contains the latest version of previous releases,
  which are still under active maintenance. Format: ```<version>-maint```
- **development:** Unstable, contains new code for upcoming releases. Format: ```<version>-dev```
- **archive:** Stable, immutable branches for old versions that no longer change
  because they are no longer maintained.

***Submit your pull requests against `master`***

*Maintenance branches are exclusively mutable by release. When a release is*
*planned, a development branch will be created and commits from master will*
*be cherry-picked into these by maintainers.*

## License ⚖️
Litemoney Core is released under the terms of the MIT license. See
[COPYING](COPYING) for more information.
