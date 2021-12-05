# The Ergo Protocol

Ergo provides a platform for developers to build the most advanced non-custodial financial contracts in the world. Allowing true peer to peer, decentralised, grassroots finance.

With a research-driven but practical development model, Ergo has prioritized useful features without compromising on security. 

*Ergo*, **a resilient platform for contractual money**

Below you can dive deeper into some of the most important components of Ergo. 

## [The Manifesto](https://ergoplatform.org/en/blog/2021-04-26-the-ergo-manifesto/)                                                      
> Cryptocurrency should provide tools to enrich ordinary people. Small businesses that are struggling to make ends meet, not big depersonalized financial capital.

## [Autolykos](/dev/protocol/autolykos)

*Autolykos* is the the underlying Memory-hard ASIC-resistant **Proof of Work** (PoW) algorithm oriented towards GPUs. 

## [eUTXO](/dev/data-model/box)

Ergo is a **UTXO** based blockchain with Proof-of-Work consensus. In this aspect, it is similar to Bitcoin. Ergo uses standard **Elliptic Curve** Cryptography with the same curve as Bitcoin (`Secp256k1`). Unlike Bitcoin and similar to Cardano, Ergo uses a so-called "extended-UTXO model," which implies UTXOs with the ability to contain arbitrary data and sophisticated scripts. 

Ergo's Smart contracts have a unique **data input** concept, which enables a radically different approach to provide robust, flexible cryptography using easy, safe scripting on privacy-centric **Sigma Protocols** (non-interactive zero-knowledge proofs). 


## [ErgoScript](/dev/scs/ergoscript)


Smart contracts are written in a high-level language called [ErgoScript](/dev/scs/ergoscript) with the ability for **Turing complete** smart contracts as demonstrated in [this peer-reviewed paper](https://arxiv.org/pdf/1806.10116v1.pdf).

Ergo provides **superior support for real-world financial agreements**. It does this through:

1. Support for [multi-stage contracts](/dev/scs/multi) 
2. A simple high-level language, ErgoScript, enabling clear descriptions of contractual logic
3. Support for formal verification of contracts, bringing improved security guarantees (Ergo Platform deployed its [first formally verified p2p crowdfunding contract](https://twitter.com/chepurnoy/status/1239936086106935296) just three months after the network launched)
4. Easy Oracle creation
5. Native support for complex signature schemes

Creating financial contracts on the blockchain isn’t just about the functionality. It’s about making that functionality safe and accessible, as well as powerful. 


### [Sigma Protocols](/site/dev/scs/sigma/index.html)

The cryptographic part of ErgoScript is based on **Sigma Protocols** and naturally supports threshold `m-of-n` signatures, ring signatures, and more. Keeping all this in mind, we expect ErgoScript and Ergo's design to be uniquely useful as **Contractual Money** with countless possible applications. 

## [NIPoPoWs](/dev/protocol/nipopow)

Extended support of light nodes makes Ergo friendly for end-users, allowing them to run contracts on common devices such as mobile phones without centralized intermediaries. 

**Non-Interactive Proofs of Proof of Work** ([NIPoPoWs](https://nipopows.com/)) are essential for two reasons: Light Clients and Side Chains. These two components are essential for clients and nodes to facilitate easier onboarding to the blockchain. A decentralized network is inherently inefficient because of the randomness mechanism in a synchronous network; that is to say, every time a transaction (TX) occurs on the network, a couple of random nodes must process the TX to prove and secure its reliability. When put into perspective, that is an enormous task on a global scale. There can be billions of transactions, and it is plausible that many of those are from contributors operating with low bandwidth.



## [Storage Rent](/dev/protocol/rent)
Another unique feature of Ergo is the concept of storage-rent, which is the ability of miners to take out a small amount of Ergs from boxes that have remained unspent for four or more years (the box is spent, and a new box is created with the lower value). This allows Ergo to avoid long-term bloat of the UTXO set.


## [Scaling](/dev/protocol/scaling)

The scaling aspect in Ergo Platform's design has been a high priority since the mainnet launch. Scalability refers to the efficient use of computational resources and high throughput. Ergo's design is built on the extended UTXO model with its novel language, ErgoScript, relying on peer-reviewed academic research. With years of research, Ergo developed various features such as stateless clients, NIPoPoWs and UTXO based smart contracts.



## Long-Term Vision

- [Long-term vision for Ergo](https://www.ergoforum.org/t/long-term-vision-for-ergo/2629) ~ 26 Sept, 2021

## Audit

- [Audit](../protocol/audit.md)