# Overview of public Ethereum networks

The [Ethereum](https://ethereum.org/?azure-portal=true) protocol is made up of multiple public networks. Different Ethereum networks can have different properties, uses, functionality and consensus mechanisms. There are four different test networks, called testnets, and one production network, called mainnet.

## An overview of mainnet

[Mainnet](https://ethereum.org/en/glossary/#mainnet), short for "main network" is the one real public Ethereum blockchain. Applications that are deployed to the mainnet can exchange and use information and interact with one another.

Once deployed, the applications can leverage the full potential of decentralized blockchain. There is no centralized authority and mainnet is fully decentralized. There can be different types of tokens and applications deployed to mainnnet. Once deployed on the mainnet, transactions are immutable and cannot be changed. In addition, each transaction has real costs associated with it which requires actual Ether (ETH). All blocks on the Ethereum mainnet can be viewed using [Etherscan](https://etherscan.io/) which shows the latest mined blocks and transactions. All blocks can be inspected.

:::image type="content" source="media\etherscan.png" alt-text="Screenshot showing the homepage of Etherscan":::

## Ethereum Testnets, Faucets and Deployment

Deploying directly to mainnet is not recommended and very high risk. There are four public testnets, each with a different deployment method and process. They are used to stage and test applications in a live public environment prior to deploying to the mainnet.

Testnets either use [Proof of Work (PoW)](https://www.investopedia.com/terms/p/proof-work.asp?azure-portal=true) or [Proof of Authority (PoA)](https://academy.binance.com/en/articles/proof-of-authority-explained/?azure-portal=true) consensus protocols to determine how new blocks of transactions are added to the network. With PoW, miners must solve a cryptographic puzzle in order to mine a new block and decide which transactions are part of that. With PoA, block validators get tto decide which transactions become part of a block by verifying their identity.

 Most testnets require that test ether that is accessed from what are called *faucets*. Using a faucet protects the testnet from spam attacks since the ether is controlled by trusted parties. This has become the primary way to acquire ether for a specific testnet. The community manages these public test networks for the benefit of developers and testing.

## Testnet Comparison

Let’s take a look at the different [Ethereum testnets](https://ethereum.org/en/developers/docs/networks/#testnets) and associated properties.

### [Ropsten](https://ropsten.etherscan.io/?azure-portal=true)

Ropsten is a PoW consensus protocol, closest to mainnet in functionality. Named after a Swedish subway station and has been around since 2016. It is said to have the best reproduction of the conditions on the the mainnet, and can be used with all clients.

- More details:
  - Supports Geth and OpenEthereum clients
  - Block time: 30 seconds or less
  - Faucet: [https://faucet.ropsten.be/](https://faucet.ropsten.be/)
  - Explorer: [https://ropsten.etherscan.io/](https://ropsten.etherscan.io/)
  - GitHub: [https://github.com/ethereum/ropsten](https://github.com/ethereum/ropsten)

### [Kovan](https://kovan-testnet.github.io/website/?azure-portal=true)

This PoA testnet is named after a subway station in Singapore. Ether can't be mined. It has to be requested from the faucet and is controlled by trusted parties. Because of this property, it is immune to spam attacks.

- More details:
  - Supports Geth and OpenEthereum clients
  - Block time: 4 seconds
  - Faucet: [https://faucet.kovan.network/](https://faucet.kovan.network/)
  - Explorer: [https://kovan.etherscan.io/](https://kovan.etherscan.io/)
  - GitHub: [https://github.com/kovan-testnet/proposal](https://github.com/kovan-testnet/proposal)

### [Rinkeby](https://www.rinkeby.io/?azure-portal=true)

PoA testnet started by the Ethereum team in April 2017 is named after a metro station in Stockholm.

- More details:
  - Only supports [Geth](https://geth.ethereum.org/?azure-portal=true) client
  - Block time: 15 seconds
  - Faucet: [https://faucet.rinkeby.io/](https://faucet.rinkeby.io/)
  - Explorer: [https://rinkeby.etherscan.io/](https://rinkeby.etherscan.io/)
  - GitHub: [https://github.com/ethereum/EIPs/issues/225](https://github.com/ethereum/EIPs/issues/225)
  - Website: [https://www.rinkeby.io](https://www.rinkeby.io)

### [Görli](https://goerli.net/?azure-portal=true)

PoA cross-client testnet and named after a Berlin subway station. This testnet has the goal of being both widely usable across various clients. It is robust enough to guarantee consistent availability and was started by the Goerli Initiative in 2018.

- More details:
  - Supports multiple clients like Geth, Pantheon, Nethermind, and OpenEthereum
  - Block time: 15 seconds on average
  - Faucet: [https://faucet.goerli.mudit.blog/](https://faucet.goerli.mudit.blog/)(Need to request the developers)
  - Status Dashboard: [https://stats.goerli.net/](https://stats.goerli.net/)
  - Explorer: [https://goerli.etherscan.io/](https://goerli.etherscan.io/)
  - GitHub: [https://github.com/goerli/testnet](https://github.com/goerli/testnet)
  - Website: [https://www.goerli.net](https://www.goerli.net)

Ropsten is said to be the testnet that is as similar to mainnet and was historically the first major testnet. Kovan, Goerli and Rinkeby are stable and have increased usage. Prior to deploying to mainnet, it’s advised to deploy to and test on multiple testnets.

## Clients and API's for deploying to **Testnets** and **Mainnet**

Ethereum is designed to offer different clients, developed by different teams using different programming languages. This makes the network stronger and more diverse. The ideal goal is to achieve diversity without any client dominating to reduce any single points of failure.

### Clients

Below is a summary of some common [Ethereum clients](https://ethereum.org/en/developers/docs/nodes-and-clients/#clients):

[**Geth Client**](https://geth.ethereum.org/?azure-portal=true)

Go Ethereum (Geth for short) is one of the original implementations of the Ethereum protocol. Currently, it is the most widespread client with the biggest user base and variety of tooling for users and developers. It is written in Go, fully open source and licensed under the GNU LGPL v3.

[**OpenEthereum**](https://github.com/openethereum/openethereum)

OpenEthereum's goal is to be the fastest, lightest, and most secure Ethereum client. We are developing OpenEthereum using the Rust programming language. OpenEthereum is licensed under the GPLv3 and can be used for all your Ethereum needs.

[Nethermind](https://nethermind.io/)

Nethermind provides the world's fastest .NET Ethereum Client and P2P Data Marketplace, along with consulting services for those looking to build Ethereum blockchain solutions.

### APIs

[Infura](https://infura.io/?azure-portal=true)

The Infura API suite provides instant access over HTTPS and WebSockets to the Ethereum and IPFS networks. It provides a simple, easy to use interface for connecting to the endpoints of all testnets. Infura supports both **Truffle Suite** and the **VS Code Blockchain Development Kit for Ethereum.**

[MetaMask](https://metamask.io/?azure-portal=true)

When deploying to either a testnet or mainnet , the MetaMask client provides a robust interface and wallet for connecting to and interacting with Ethereum blockchains.

Using MetaMask to send Ether and tokens on a testnet is straightforward. As we've seen in previous tutorials, the client provides an easy interface to select and use different Ethereum networks. For interacting with development networks, it's simple with MetaMask to connect to Localhost 8545 or Custom RPC to connect with Ganache and Truffle. Similarly, MetaMask has predefined connections to the public testnets and mainnet. If connecting to mainnet, be careful to secure your private key since real Ether is being used.