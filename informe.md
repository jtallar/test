# Chainlink - A bridge to the real-world, a bridge to the future.

<br>

<br>

# 1. Introduction

Chainlink is a **decentralized oracle network** that enables smart contracts to securely interact with real-world data and services that exist outside of blockchain networks. 
By combining on-chain and off-chain components, Chainlink is able to **connect the outside world with any given blockchain without losing its end-to-end determinism**. 
In this article, we will dive deep into the problem, how Chainlink works, the LINK token, their community, and the company behind the project, among other Chainlink related topics.

![Chainlink in a nutshell](https://coincentral.com/wp-content/uploads/2018/01/ChainLink4.png)

For short, Chainlink connects real world data to the blockchain in a decentralized manner.

Let´s begin...

<br>

# 2. The Problem

## 2.1. Retrieving Off-Chain Data

The blockchain industry has been growing a lot in the last few years and smart contracts are one of the main reasons why.
Smart contracts have the ability to revolutionize multiple processes because of the pure deterministic logical method by which they issue funds and perform actions. 
**This means that outcomes are predictable - given the same input, the output will always be the same**.

But most of the time, some of the information needed by the contract to make these critical decisions is not on-chain and accessible at the time it needs it. There is a need for smart contracts to **connect to the outside world** to do more interesting things, like:
+ Getting market data for DeFi. 
+ Sports results.
+ Weather conditions.
+ And much more! 

However, blockchain’s security is derived from a decentralized network of independent validators who intentionally limit their connection to the outside world. And transactions need to be **validated by all nodes**, who need to be able to reproduce them in a deterministic way.

## TODO IMAGE HERE OF THE EXAMPLE

Let´s show an example,
1. A smart contract calls an API directly.
2. The other nodes need to call the API again when validating this transaction.
3. Every time this transaction is replayed the **response from the API would probably differ**, because of :
  + Changes in the API.
  + Changes in the actual data.
  + Or even hacks. 
4. All nodes will try to reach a consensus unsuccessfully and thus the transaction **will not be validated**. 

This is why smart contracts require an additional piece of infrastructure known as **oracle** to securely retrieve data from the outside world.

<br>

## 2.2. Oracles

What is a blockchain oracle? A blockchain oracle is a secure piece of middleware that **facilitates communication between blockchains and any real world off-chain system**. 
This includes any type of datasource that could be needed to provide data to smart contracts on-chain. 

> The data supplied by oracles will control smart contracts and therefore **billions of dollars in value**, so it needs to meet the highest possible standards. 
Smart contracts can only execute with high quality results with high quality data. 
If this is not the case, bad results are expected. **Garbage in, garbage out**.

## TODO IMAGE HERE OF THE ACTIONS BELOW

To connect the blockchain to the real world, the oracle system needs to be operating both on and off the blockchain simultaneously. The on-chain component is used for:
+ Establishing blockchain connections.
+ Listening for requests.
+ Broadcasting data.
+ Extracting blockchain data.
+ Performing any computation needed on the blockchain. 

The off-chain component is for:
+ Processing requests.
+ Retrieving and formatting external data.
+ Performing off-chain computation. 
+ Reporting the external data on the chain in a transaction, guaranteeing that the blockchain **has all the information it needs to verify itself**.

But this brings a whole new problem to the scene.

<br>

## 2.3. The Oracle Problem

The oracle problem is defined as the **security, authenticity, and trust conflict** between third-party oracles and the trustless execution of smart contracts. 
This problem goes around a very simple limitation previously discussed - blockchains cannot pull in data from or push data out to any external system as built-in functionality. 
As such, blockchains are isolated networks, a key property which makes the system extremely secure and reliable. 
**But data has to come from somewhere**. 

If we imported data through a centralized oracle or datasource, we are essentially removing one of the best benefits of blockchain, nullifying the advantages of decentrality. 
The entire point of using smart contracts is to achieve determinism programmatically as opposed to probabilistic execution carried out by a human being. 
To fulfill this, the blockchain **cannot have any single point of failure**, a feature that must apply to the oracle to maintain end-to-end determinism. 

![A centralized oracle as SPF](https://2eguue18ymh52albtja2v96c-wpengine.netdna-ssl.com/wp-content/uploads/2020/08/Slides-02-1536x686.png)

> Moreover, this oracle itself would now **retain an enormous amount of power** over the entire execution of smart contracts, as the data provided determines how the contract executes. 
Even if the oracle operator operates with the best intentions, they are still subject to mistakes, attacks and hacks.

To overcome these shortcomings, oracles need to create the same security and reliability guarantees of a blockchain, applied to this different problem. This is where Chainlink comes in.

<br>

# 3. The Idea

## 3.1. What is Chainlink?

Chainlink is a decentralized oracle network that enables smart contracts to securely interact with real-world data and services that exist outside of blockchain networks. 
Their goal is to provide **reliable tamper proof inputs and outputs** on multiple networks that can be used to build complex and valuable smart contract ecosystems. 

They can supply the **definitive truth** about the external world by leveraging the same reliable decentralized infrastructural concept that makes blockchain work, securely connecting the world’s existing infrastructure to the emerging blockchain’s that aims to redefine it.

Chainlink unlocks the creation of what they defined as **hybrid smart contracts** (or hybrid contracts) in the Chainlink 2.0 whitepaper. 
These are applications that consist of a smart contract - code that runs exclusively on the blockchain, and decentralized oracle networks - secure off-chain services that support the smart contract. 
Chainlink decentralized oracle networks provide multiple off-chain services to existing and future blockchain networks. 
The two components interact with each other seamlessly and securely to form a single hybrid smart contract application.

The Chainlink ecosystem includes hundreds of decentralized applications (dApps), blockchains, node operators, and data providers, as well as an expansive research and open-source development community. 
Chainlink has become the **default solution for the DeFi space**. As Chainlink is a permissionless framework for building oracles, anybody can join the network at any time and immediately start contributing to the growing ecosystem.

![Chainlink's idea](https://2eguue18ymh52albtja2v96c-wpengine.netdna-ssl.com/wp-content/uploads/2020/11/chainlink-diagram-1536x517.png)

> The Chainlink network is highly flexible as it is an inherently **blockchain-agnostic framework**, acting as a universal blockchain abstraction layer. 
Users can leverage Chainlink to transmit any kind of data to and from any blockchain environment as desired. 

<br>

## 3.2. Use Cases
Chainlink oracles bring solutions to multiple industries that are already using smart contracts. These are some of the main use cases enabled by Chainlink:

+ ***Decentralized Finance (DeFi)***
  + Picing assets.
  + Accessing interest rates and verify collateralization. 
  + Issuing loans at fair market value, automating the issuance of dividends and settling an options contract.
+ ***Insurance***
  + Weather data (amount of rainfall, temperature, or other evaluators set in the policy) in the Arbol crop insurance market. 
  + This settles parametric crop insurance in a fair and timely manner according to the provided data.
+ ***Gaming***
  + Randomness solution called Verifiable Random Function (VRF).
  + It generates randomness and delivers it to the smart contract in a way where users can prove it is fair and unbiased.
+ ***External Payments**
  + Facilitate payment services by pushing outputs from smart contracts to external APIs. 
  + Connecting smart contracts to existing banking systems, credit card providers and established payment networks.
+ ***Sports***
  + Decentralized, tamper-resistant source of external data to verify sporting outcomes by aggregating data from reliable web APIs. 
  + This data can be used to trigger the settlement of a prediction market or sports bets, and the payment to the winners.
+ ***Supply Chain***
  + Connect supply chain smart contracts to web APIs, cloud networks and multiple real-world sensors (IoT sensors, RFID devices, etc). 
  + This data can be used as a golden source of truth to trigger payments and transfers of data between parties.

  <br>

# 4. How it Works

A Chainlink network is composed of a collection of Chainlink nodes with registered Job specifications which live off-chain. They can carry out job executions coordinated by the on-chain oracle contracts, which use **LINK tokens** as an incentive for the Chainlink node operators to serve clients via the Chainlink client smart contracts. Next is the complete workflow that will be covered in the following sections. 

![An example of Chainlik's complete workflow](https://assets-global.website-files.com/5dfc18aeef0cf97edeb5ccd2/5e46e8f698804c8064a5f871_Chainlink.png)

<br>

## 4.1. On-Chain Components

### 4.1.1. Oracle Contracts

These contracts are the first on-chain components and **work as the core interface** for dApp developers to interact with the off-chain Chainlink oracle nodes that provide data. They are responsible for:
1. Receiving on-chain data requests from the consumer contracts.
2. Publishing EVM events to be picked up by the appropriate Chainlink oracle node for off-chain processing. 
3. Once the job is finished, routing the executed data job results back to the requesting contract. 
4. Maintainin job IDs determining which Chainlink node can handle each type of data request.
5. Locking up the LINK deposit and facilitating LINK transfers to jobs.

> It is useful to have more than one active oracle contract in the same blockchain network. 
This allows consumers contracts to choose which oracle contract to send job requests to and allows off-chain Chainlink nodes to register with one or many on-chain oracle contracts, deciding what jobs they will pick.

### 4.1.2. Consumer or Client Contracts

The second on-chain components -created by dApp developers- **consume oracle data feeds** from the Chainlink network and integrate the core library functionality. 
They must implement code to identify and interact with LINK token contracts and oracle contracts. They: 
1. Build job requests, choosing an oracle contract address and a specific job ID to use to grab data. 
2. They then handle the callback function for the response data to be sent to.

> The job ID defines the specifics of the data job requested, as it identifies the off-chain Chainlink node to handle the request. 

### 4.1.3. LINK Token Contracts

The last on-chain components are LINK token contracts. 
These contracts implement the main functionality and supply for the LINK cryptocurrency, which is an **ERC677 token**. 
This extension of ERC20 allows tokens to be transferred to contracts and have the contract trigger logic for how to respond to receiving tokens **within a single transaction**. 

Initialy this contract minted 1 billion LINK tokens that make up the total supply and handles the core operations on the LINK cryptocurrency - transfer, approval, supply check, etc. 
LINK tokens are **used by oracle contracts as an incentive** for Chainlink node operators to execute the specified jobs and are also the financial deterrent for them to falsify data or accept jobs they can’t deliver.

<br>

## 4.2. Off-Chain Components

### 4.2.1. Nodes

Chainlink’s off-chain network is composed of multiple independently operated Chainlink oracle nodes that **carry out the requested job execution**. Chainlink core nodes:
1. Connect to the chain.
2. Watch for their job IDs.
3. Handle requests for data. 
4. Submit the requested data back to the consumer contracts on-chain, earning LINK tokens for their work.

> The core nodes need a blockchain node or a connection that allows the node to listen for blockchain events containing their job ID’s and broadcast transactions back to the blockchain.

### 4.2.2. Data Sources & Adapters

The other off-chain components are the **external data sources** -data repositories, databases and APIs- that the oracle will use to fulfill the data requests from the contracts on-chain. 

And lastly, **custom data adapters** allow Chainlink nodes to access a wide variety of data sources, formatting and modifying data for specific purposes or even adding sensitive password keys. 
These give the nodes a high degree of flexibility, keeping API credentials off-chain and separate from the node itself.

> Oracle nodes are built to aggregate data from multiple data sources to get a more trustworthy dataset.

<br>

# 5. Technical Details

## 5.1. Whitepapers

Steve Ellis and Sergey Nazarov published Chainlink’s original white paper **“Chainlink. A Decentralized Oracle Network”** in September 2017 with Ari Juels, an advisor to the company. 
This paper presented Chainlink as a decentralized oracle network, described its architecture and security, and layed out possible future improvements.

Four years later, the same authors -along with other Chainlink Labs advisors and researchers- published a second white paper **“Chainlink 2.0: Next Steps in the Evolution of Decentralized Oracle Networks”**. 
This paper outlines how Chainlink decentralized oracle networks can go on to create a decentralized metalayer that enhances smart contracts with off-chain computation, in addition to the external data that Chainlink already provided as a decentralized oracle solution. 
This new off-chain computation layer is the base of new Chainlink decentralized services designed for smart contracts such as Chainlink Keepers -maintenance of functions like harvesting yield and triggering liquidations- and an enhanced version of Chainlink VRF.

<br>

## 5.2. Oracle Implementation

Chainlink has been popular in the community where, unlike other Oracle designs that rely on a centralized party to be trusted as a gateway, is built on a **network of independent node operators** to offer unique integrations. 

In order to allow communication between the blockchain-based smart contracts it services and external data sources, Chainlink follows an innovative 3-step process:
1. ***Oracle Selection***
   1. A Chainlink user drafts a Service Level Agreement (SLA) specifying a certain set of data requirements. 
   2. The Chainlink software uses this SLA to match the user with the most appropriate oracles. 
   3. The user submits the SLA and deposits their LINK tokens in an Order-Matching contract, which accepts bids from oracles.
2. ***Data Reporting***
   1. The oracle connects with the external data sources to obtain the requested real-world data. 
   2. The data is then processed by the oracles and sent back to the contracts utilizing the Chainlink service.
3. ***Result Aggregation***
   1. The result of the data is collected by the oracles and returned to what’s known as an Aggregation contract. 
   2. The Aggregation contract:
      1. Takes the data points.
      2. Assesses the validity of each data point.
      3. Returns a weighted score, using the sum of all the data received, to the user (smart contract).

In summary, Chainlink is able to **bridge on-chain data requests with off-chain data** by having the Chainlink node listen to specific logs (requests), parsing data out of the logs, running a sequential job pipeline, and then sending the result of the pipeline to the requesting smart contract.

<br>

## 5.3. Token & Nodes

There are two tipes of contracts associating the nodes and its token handling,
1. ***Requesting Contract*** 
   + Its holders use a LINK token to pay Chainlink node operators for their work. 
   + Prices are set by the Chainlink node operator, based on demand for the data to provide. 
   + Node operators must deposit LINK with Chainlink to demonstrate their commitment to the network and incentivize good service.

2. ***Chainlink Reputation Contract*** 
   + Considers the size of a node’s stake (among other criteria) when matching nodes with requests. 
   + Nodes with a greater stake are more likely to be chosen to fulfill requests (and thus earn LINK tokens).
   + The Chainlink network also punishes faulty or dishonest nodes by taxing the node's stake in LINK for poor service.

<br>

## 5.4. Deploying Client Smart Contracts

The Chainlink smart contracts are deployed on the blockchain and used by other smart contracts to initiate requests and receive off-chain data. 
As the implementation is based on the Ethereum blockchain, the smart contracts are using the Solidity programming language. 

> If a smart contract wants to use Chainlink to request off-chain data, must extend the subclass of the Chainlinked smart contract `ChainlinkClient`. 
This contract provides the necessary imports of functions, data structures, and other Chainlink smart contracts.

Let's see a real life example of a smart contract using Chainlink to request API data (of course the values are all harcoded).

```java
pragma solidity ^0.8.7;
import "@chainlink/contracts/src/v0.8/ChainlinkClient.sol";

contract APIConsumer is ChainlinkClient {
    using Chainlink for Chainlink.Request;
    uint256 public volume;
    address private oracle;
    bytes32 private jobId;
    uint256 private fee;
    
    constructor() {
        setPublicChainlinkToken();
        oracle = 0xc57B33452b4F7BB189bB5AfaE9cc4aBa1f7a4FD8;
        jobId = "d5270d1c311941d0b08bead21fea7747";
        fee = 0.1 * 10 ** 18; // (Varies by network and job)
    }
    
     // Create a Chainlink request to retrieve API response, find the target
    function requestVolumeData() public returns (bytes32 requestId) 
    {
   	Chainlink.Request memory request = buildChainlinkRequest(jobId, 
		address(this), this.fulfill.selector);
        
       // Set the URL to perform the GET request on
	request.add("get", "https://min-api.cryptocompare.com/data/pricemultifull?fsyms=ETH&tsyms=USD");
              
	request.add("path", "RAW.ETH.USD.VOLUME24HOUR");
        
       int timesAmount = 10**18;
       request.addInt("times", timesAmount);
        
        return sendChainlinkRequestTo(oracle, request, fee);
    }
    
 function fulfill(bytes32 _requestId, uint256 _volume) public recordChainlinkFulfillment(_requestId)
    {
        volume = _volume;
    }
}
```

<br>

## 5.5. Running Nodes

Chainlink nodes expose a command-line interface that allows users, amonng other things, to:
+ Start the node.
+ Show all/single job run(s).
+ Create a JobSpec.
+ Begin a job run.
+ Backup the database
+ Import a key file. 

> The Chainlink nodes are written in **Golang**. This is due to its unique features, not seen in most programming languages, such as **Goroutines and channels**.

This command-line call ends up calling a `RunNode` function whose main objective is to:
1. Connect to the Ethereum blockchain.
2. Create the `ChainlinkApplication` object.
3. Authenticate with the `KeyStore`.
4. Call the `ChainlinkApplication` start method.
5. Set up the Chainlink REST API (allowing the creation of JobSpecs, bridge adapters, etc).

<br>

## 5.6. Security

Can Chainlink be hacked? If Chainlink network could be hacked, it would have probably already happened. 
The blockchain is decentralized across many independent nodes -the more nodes on the network, the higher the security. 
**If any one node is compromised, it will not compromise the others**. 

The Chainlink network is secured by a similar concept to **Proof of Stake (PoS)**, where its validator nodes stake LINK in order to obtain data contracts and be rewarded by the network. 
The incentivized rewards system dissuades network nodes against malicious or unscrupulous behavior, as does the risk of losing the LINK they have staked.

The Chainlink decentralized oracle network is powered and secured by three types of custom-designed smart contracts as well:
+ ***Aggregation Contract***
  + Collects the data from oracles.
  + Matches the most accurate results with the smart contract that needs them.
+ ***Order-Matching Contract***
  + Matches the best possible oracle with the smart contract’s service level agreement (SLA) needs.
+ ***Reputation Contract***
  + Verifies the integrity of an oracle by checking its statistics.
  > This includes the  number of completed requests, average response time, and amount of LINK tokens staked.

<br>

# 6. LINK Token

## 6.1. Summary

The LINK token is an ERC677 token that allows token transfers to contain a data payload. 
It is used to pay node operators for retrieving data for smart contracts and also for deposits placed by node operators as required by contract creators.LINK is built on Ethereum in accordance with the ERC20 standard for tokens, meaning it can be bought and sold for fiat currency or any other digital currencies. 

> The token is meant to help finance the growth of the project and is similar to Bitcoin (BTC) and Ethereum (ETH). 
Both of these cryptocurrencies work on their respective blockchains. 
**Just like BTC and ETH act as an incentive for users to mine, LINK does the same**.

The initial coin offering (ICO) raised the equivalent of **$32 million by selling 35% of the 1 billion unit supply** of its LINK cryptocurrency. 
As for the remainder of the tokens, 30% were distributed to SmartContract to be used for the development of the Chainlink blockchain and 35% went to incentivize node operators.

<br>

## 6.2. Accepted Wallets & Exchanges

As it was stated before, LINK is an ERC677 token, an **extension of the ERC20 token**. 
Tokens can be stored in **any ERC20 wallet**, as the ERC677 token retains all the functionality of an ERC20 token. 
Regardless, the most popular wallets for storing LINK are:
+ Ledger
+ Trust Wallet
+ MetaMask
+ Coinbase
+ Binance Chain Wallet

LINK is one of the most popular tokens on the market, nevertheless not all exchanges trade it. 
The most used exchanges to trade LINK tokens are:
+ Binance
+ Huobi Global
+ Coinbase Pro
+ Gate.io
+ Kraken

<br>

## 6.3. Economics

As with any token, its price and market cap highly varies every single day, so the next information is probably already outdated. 
For more up to date information, [check this link](https://coinmarketcap.com/currencies/chainlink/).
+ ***Initial Coin Offering***: September 2017, 350M tokens sold at $0.11
+ ***Max Supply***: 1,000,000,000 LINK
+ ***Circulating Supply***: 455,009,553.92 LINK
+ ***Market Cap***: $10,274,859,591

There is an interesting insight on holder statistics for the LINK token, shown in the next table. 

|       | **LINK** | **UNI** | **USDT** | **BTC** |
| :---: |   :---:  |  :---:  |   :---:  |  :---:  |
| **Top 10 Holders** | 62.03% | 53.71% | 23.35% | 5.37% |
| **Top 20 Holders** | 68.27% | 63.09% | 29.94% | 7.47% |
| **Top 50 Holders** | 75.93% | 78.99% | 37.93% | 10.72% |
| **Top 100 Holders** | 80.78% | 88.6% | 43.26% | 13.38% |

It's clear that BTC is not a token, and USDT is not quite used the same way as the rest of the tokens. But why is this? The main reason is that 60% of the supply remains under the control of the parent company (not freely traded on the market).

The actual number of users trading LINK tokens is difficult to say precisely, many users could have several wallets and execute transfers between them. The next two metrics provide a general overview of the possible number of users. 
+ ***Total Wallet Addresses***: 590,103
+ **Active Addresses (past 24hs)***: 10,403

> Just for clarification, this is not the amount of users using the technology and protocol of Chainlink, only its tokens.

<br>

# 7. The Company

## 7.1. Origins

The Chainlink network and its first version were launched in June 2017 by the for-profit company **SmartContract**. 
The founders and main members are:
+ ***Sergey Nazarov***
  + CEO and co-founder of the company. 
  + Founder of Secure Asset Exchange, a cryptocurrency exchange. 
  + Founded a completely decentralized email service, dubbed CryptoMail.
+ ***Steve Ellis***
  + CTO and co-founder of the company. 
  + Ellis worked with Nazarov on the Secure Asset Exchange platform. 
  + Worked at Pivotal Labs prior to joining the blockchain sector.
+ ***Ari Juels***
  + Advisor to the Chainlink team.
  + Along with Nazarov and Ellis, wrote Chainlink’s whitepaper. 
  + Computer science professor at Cornell Tech and the director of IC3.

<br>

## 7.2. Partnerships

In the last three years, ChainLink announced over 70+ partnerships through their social media channel.  
Some of the most outstanding partnerships and its goals are:
+ ***Google Cloud*** 
  + Simplify the develop of technologies by granting access to cloud data, among other things, on public blockchains. 
+ ***Oracle*** 
  + Help startups monetizing their APIs on the Oracle Blockchain Platform. 
+ ***Swift***
  + Support for their DLT based payments system called GPI Link (Global Payments Innovation).
+ ***Dapps Inc***
  + Help Salesforce users to obtain accurate and real-time data for smart contract management. 
+ ***Polkadot***
  + A blockchain project that wants to allow different blockchains to communicate with each other. 
  + This confirms Chainlink’s ambitions to work with as many different blockchains as possible. 
+ ***China’s National Blockchain Services Network (BSN)***
  + Obtain and arrange off-chain data.
+ ***Binance***
  + Provide on and off-chain data exchange for its DeFi platform.
+ ***Cardano***
  + Accelerate the development of its DeFi ecosystem.

> LINK price saw an average rise of 10% after each and every partnership announcement, and a massive surge of 50% within 48 hours after they announced a partnership with Google Cloud in 2019.

<br>

## 7.3. Team

Chainlink is now managed by the San Francisco based company **Chainlink Labs**. The team is composed of more than 200 employees. While the most part of the employees live in the United States, there is a portion that lives outside the of it in countries such as the United Kingdom, Germany and Singapore. This is mostly possible due to the majority of the job offers being remote.

<br>

## 7.4. Governance

Chainlink, as opposed to various other DeFi protocols, **has no governance model**. 
The oracle network is administered by the Chainlink team. 
Most decisions are made **unilaterally by them and could serve as a large centralization risk**. 
However, it’s important to note that the ecosystem functions independently from the team, which is to say that oracles are controlled by owners. 

In summary, this creates a **hybrid semi-decentralised network** with various third party-clusters, and where the community has no real power over how the Chainlink team chooses to use its ICO funds. 
LINK tokens help create self-regulating governance (of sorts) of the Chainlink network by creating economic incentives for honest behavior. 

<br>

## 7.5. Repository

As we’ve seen previously, Chainlink is an **open-source technology**, collectively developed by a large community of developers, researchers, and users who share the goal of building Chainlink into a public good for the benefit of the entire blockchain ecosystem. 

In the repository hosted on GitHub, we can find the Chainlink Golang node, currently in alpha. 
The initial implementation is intended for use and review by developers and it’s expected to form **the basis** for Chainlink's decentralized oracle network. 
Further development of the Chainlink Node and Chainlink Network will happen there. 
The current codebase is still under active development, with many of the features described in the design still coming, and can be found [here](https://github.com/smartcontractkit/chainlink).

> Currently the repo has: **16308** commits (fist one made on November 19th, 2017), **90** contributors and **79** releases.  

<br>

## 7.6. Progress Report

Chainlink is an open source project, allowing anyone to review and contribute to it. 
It has several repositories on Github with the most active repo accruing over 4,000 commits from 33 developers over the past year. 
The current codebase is still under active development as is evident by **ranking #2** in activity over the last year within the crypto space.

The Chainlink team does not give timelines or estimates for development targets. 
The **Pivotal Tracker** (constantly updated, after all Ari Juels worked there) or Github page is the user’s only ability to track the development progress.

<br>

# 8. Nowadays

## 8.1. Indicators & Metrics 

As of today, according to [Chainlink’s Market](https://market.link), Chainlink has **322 active nodes and 2885 data feeds** -real-world market price providers- across every compatible blockchain.
Most nodes and feeds are connected to the Ethereum blockchain, where Chainlink first deploys their features. 
In fact, all the features described in the [Contract Developers documentation](https://docs.chain.link/) are available in the Ethereum network, with only some of them are also live in other blockchains like Binanece Smart Chain and Solana. 
Data feeds is the most supported feature, available at eleven different blockchains.

If we analyze some of the metrics provided in the market, we can see that there have been around **180 average daily transactions** on Ethereum’s Mainnet in the last seven days, but almost **50 thousand average daily transactions** on xDai's Mainnet. Lots of DeFi dApps are deployed on xDai (like SushiSwap and Honeyswap) and at the moment, DeFi is the industry where we can find most integrations with Chainlink, using Chainlink price feeds to ensure that prices across their products remain stable and accurate.

![Chainlink's integrations per year](https://drive.google.com/file/d/1JObKj9pYz3_RLSdtPGQXOZL82tPGarQE/view)

> If we count the number of integrations created each year, we can see that the number is almost **duplicating year after year**.

<br>

## 8.2. News

Latest 5 different Chainlink news (from newer to older):
- [$1.45 Billion in LINK Bought by Chainlink Whales in Single Week](https://u.today/145-billion-in-link-bought-by-chainlink-whales-holding-1-to-10-million-coins-in-single-week)
- [Cardano, Chainlink Primed to Dip Despite Partnership](https://cryptobriefing.com/cardano-chainlink-ready-dip-despite-recent-partnership/?utm_source=main_feed&utm_medium=rss)
- [Cardano (ADA) Partners With Chainlink (LINK) for Oracle Services](https://beincrypto.com/cardano-ada-partners-with-chainlink-link-for-oracle-services/)
- [Alchemix integrates with Chainlink to make DeFi loans a ‘set and forget’ thing](https://coinmarketcap.com/headlines/news/alchemix-integrates-with-chainlink-to-make-defi-loans-a-set-and-forget-thing/)
- [AutoShark Integrates Chainlink VRF to Enable Randomized NFT Rarity Boosts](https://www.bsc.news/post/autoshark-integrates-chainlink-vrf-to-enable-randomized-nft-rarity-boosts)

<br>

## 8.3. Hacks

Currently the Chainlink project hasn’t suffered many attacks from hackers, the most recent one was on the nodes. 
This attack exploited the way in which nodes respond to queries and involved the use of a token tied to network transaction costs. 
**Chainlink confirmed the attack** and described it as a “failed attempt” to spam the network, more info [here](https://www.theblockcrypto.com/post/76986/chainlink-nodes-attack-eth). 

> Chainlink offers a [bug bounty program](https://hackerone.com/chainlink?type=team) where hackers can get paid for the bugs they find, according to the severity of the exploit.

<br>

# 9. Community

## 9.1. Social Network & Profiles

Social networks are a good measurement of the community -besides the team- surrounding the project. 
The community gathers in the next places:
+ ***Twitter***: 505.000 followers
+ ***Telegram***: 39.174 - 2.000 online average
+ ***Discord***: 23.392 - 2.000 online average
+ ***Reddit***: 67.800 members - 100 online

> And of course there is a LinkedIn account for those looking to work on the Chainlink project itself.

In all the social networks mentioned above the users communicate in English, mostly because it is a San Francisco based company. There is usually a fast response time in all the channels, and it's composed mostly by chainlink and crypto enthusiasts, team members, and referent people on the crypto scene.

<br>

# 10. Competitors

Chainlink is not the only project that is trying to solve the Oracle problem in a decentralized manner. Here are some of the top Chainlink competitors.

<br>

## 9.1. Band Protocol
[Band Protocol](https://bandprotocol.com/) is another **blockchain-agnostic data oracle** platform that aggregates and connects trusted off-chain information provided by community-managed data providers to smart contracts. 

BAND’s data feeds are **community-managed data sources** that provide a framework for dApp users and developers to moderate, operate, and manage the data sources themselves, which ensures that the data is trusted and reliable. 
The community can select certain providers through voting, which will then rise in the ranking, making data more trustworthy in the long run. 
This way, the **decision-making power is transferred to the users** rather than depending on cooperations and data providers.

<br>

## 9.2. Tellor
[Tellor](https://www.tellor.io/) is an Ethereum based oracle service, **leveraging a mining mechanism** to have miners compete to deliver data and reward them with minted tokens. 
Inputs to a data series are secured by a hybrid Proof-of-Work / Proof-of-Stake consensus mechanism and by choosing the median of the first five values received. 
Contrary to Chainlink, Tellor is **only aimed at the Ethereum** blockchain and is more focused on **security and decentralization** and less on speed.

<br>

## 9.3. UMA
[UMA](https://umaproject.org/) has created a **decentralized “Optimistic oracle”** by leveraging game theory. 
Anyone can push an answer on-chain and there will only be a dispute if it’s wrong, meaning that answers are delivered quickly. 
There are three actors in this system: the requester -the contract requesting a price-, the proposer -an off-chain actor that proposes a price-, and the disputer -an off-chain actor that is able to dispute prices they disagree with.

<br>

# 10. The Future

## 10.1. Chainlink 2.0 and Its Expected Features

The release of Chainlink’s Whitepaper 2.0 written in April 2021 addresses the limitations of smart contracts with several solutions in mind including:
+ On-chain and off-chain **securely composed computations**.
+ **Removing complexity** on protocols and systemic boundaries for simple functionality.
+ **Warranting scalability** by meeting demand for throughputs and latencies from decentralized systems.
+ **Providing privacy** for data while staying transparent through the blockchain.
+ **Fair Sequencing Services**.
+ Lowering the need for trust for smart contracts and other oracle-dependent systems.
+ Designing an **incentive-based system** for nodes based in Decentralized Oracle Networks (DONs moving forward) to promote good behavior for the overall health of the network.

> This is a general recap of all the new features and solutions the 2.0 Chainlik’s version will (hopefully and eventually) provide. 

<br>

# 11. Final Thoughts

Oracle platforms like Chainlink are really important for the future of the blockchain industry. 
The blockchain realm needs oracles if it wants to see legitimate adoption and have a chance of accomplishing its promised goals. 
And to fill this necessity, Chainlink has created a truly decentralized oracle provider that can be used without losing all the other advantages of blockchain.

Chainlink has grown a lot in these four and a half years since its first white paper was published. 
As of today, it is the absolute leader of the oracle market and its competitors are far off their numbers, with most of them just trying to emulate Chainlink’s success. 
Chainlink is widely used in DeFi applications, with almost half of its integrations used in that industry. 
Data Feeds are available in multiple blockchains and lots of dApps use them to retrieve the latest asset prices.

On the other hand, we can find some negative aspects regarding Chainlink. 
With the release of its second paper early this year, we think some of the proposed features are a bit out of scope. 
Even though some things actually need to be computed off-chain (like randomness with VRF), we don’t believe moving so much computation off-chain will have a huge adoption by the community.

Another point against Chainlink is its governance and token distribution as discussed above. 
Although the ecosystem functions are independent, the oracle network is administered entirely by the Chainlink team and most of LINK’s supply remains under the company’s control.

Its blockchain-agnostic promise has only been fulfilled in some of its features, as many of them are only running on Ethereum’s blockchain. 
Their decentralized oracle networks are designed in a blockchain-agnostic way, but they haven’t figured out a way of completely taking advantage of this.

All in all, we believe Chainlink has taken its place as the main decentralized oracle in blockchain and still has lots of potential to continue growing. 
Its drawbacks are negligible compared with the huge value it provides to blockchain as a whole. 

Chainlink has actually become the bridge between the blockchain and the real-world and it has helped blockchain move one step closer to success. 
One step closer to the future.


<br>

# 12. Aditional Resources

## 12.1. Implementation
+ [Chainlink Original Whitepaper](https://research.chain.link/whitepaper-v1.pdf?_ga=2.252736841.1971981138.1632594158-16702909.1632594158)
+ [Chainlink 2.0 Whitepaper](https://research.chain.link/whitepaper-v2.pdf?_ga=2.252736841.1971981138.1632594158-16702909.1632594158)
+ [Chainlink Smart Contract Documentation](https://docs.chain.link)
+ [Chainlink Market](https://market.link/)
+ [Chainlink FAQs](https://chain.link/faqs)
+ [Chainlink GitHub Repository](https://github.com/smartcontractkit/)
+ [Building DeFi Applications](https://chain.link/solutions/defi)
+ [Chainlink Pivotal Tracker](https://www.pivotaltracker.com/n/projects/2129823)
+ [Chainlink Ecosystem](https://www.chainlinkecosystem.com/ecosystem/)

## 12.2. Social
+ [Twitter](https://twitter.com/chainlink)
+ [Telegram](https://t.me/chainlinkofficial)
+ [Discord](http://discord.gg/aSK4zew)
+ [LinkedIn](https://www.linkedin.com/company/chainlink-labs/)
+ [Reddit](https://www.reddit.com/r/Chainlink/)
+ [Newsletter](https://chn.lk/newsletter)

## 12.3. Economics
+ [CoinMarketCap](https://coinmarketcap.com/currencies/chainlink/)
+ [Market](https://market.link/)

<br>

# 13. References

+ https://research.chain.link/whitepaper-v1.pdf?_ga=2.252736841.1971981138.1632594158-16702909.1632594158 
+ https://www.youtube.com/watch?v=tIUHQ7sDoaU&ab_channel=Chainlink 
+ https://www.youtube.com/watch?v=ZJfkNzyO7-U&ab_channel=Chainlink 
+ https://ethereum.stackexchange.com/questions/301/why-cant-contracts-make-api-calls 
+ https://www.youtube.com/watch?v=m_1uDhsnghw&ab_channel=Hashoshi 
+ https://blog.chain.link/what-is-the-blockchain-oracle-problem/ 
+ https://blockonomi.com/oracles-guide 
+ https://encyclopedia.pub/3718 
+ https://blog.chain.link/what-is-chainlink/ 
+ https://blog.chain.link/hybrid-smart-contracts-explained/ 
+ https://chain.link/faqs
+ https://blog.chain.link/44-ways-to-enhance-your-smart-contract-with-chainlink/
+ https://www.kaleido.io/blockchain-blog/how-chainlink-works-under-the-covers
+ https://github.com/ethereum/EIPs/issues/677
+ https://research.chain.link/whitepaper-v2.pdf?_ga=2.252736841.1971981138.1632594158-16702909.1632594158 
+ https://blog.chain.link/chainlink-2-0-lays-foundation-for-adoption-of-hybrid-smart-contracts/
+ https://kriptomat.io/chainlink/
+ https://www.gemini.com/cryptopedia/what-is-chainlink-and-how-does-it-work
+ https://medium.com/coinmonks/technical-overview-of-the-chainlink-testnet-implementation-c8a0b09276d1
+ https://www.cointribune.com/en/crypto-guides/ultimate-guides-to-cryptocurrency/chainlinks-link-history/
+ https://itsblockchain.com/chainlink-partnerships/
+ https://finance.yahoo.com/news/chainlink-adoption-rates-continue-prove-151937281.html
+ https://twitter.com/top7ico/status/1291790903481454592?lang=es
+ https://medium.com/coinmonks/what-is-band-protocol-band-375063aeab3e
+ https://www.crypto-news-flash.com/crypto-influencer-3-chainlink-competitors-have-a-100x-profit-potential/
+ https://www.undervalued.top/cryptocurrency-reviews/tellor-review
+ https://medium.com/tellor/what-is-tellor-5a4ff2159dbe
+ https://medium.com/uma-project/introducing-umas-optimistic-oracle-d92ce5d1a4bc
+ https://docs.umaproject.org/getting-started/oracle
+ https://coincentral.com/what-is-chainlink-a-beginners-guide-to-decentralized-oracles/
+ https://www.cryptoeq.io/corereports/chainlink-abridged
+ https://swissborg.com/blog/what-is-chainlink 
+ https://www.kraken.com/learn/what-is-chainlink-link 
+ https://messari.io/asset/chainlink/profile 
