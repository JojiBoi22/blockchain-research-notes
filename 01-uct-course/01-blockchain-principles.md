# Module 1 – Blockchain Principles

**Course:** UCT GetSmarter – Blockchain and Digital Currency  
**Status:** Completed

---

## Key questions this module answers
- What exactly is a blockchain?
- How does it achieve consensus without a central authority?
- What are the core components that make it work?

---

## Main concepts

### 1. What is a blockchain?

**Definition**  
A blockchain is a time-stamped, immutable record of data that is managed by a decentralised network of computers. (Rosia, n.d.a)

**Distributed ledger vs traditional database**  
- A **distributed ledger** is a decentralised, shared database where transactions are recorded across multiple nodes (computers) in a network. All participants have access to the same data, and changes require consensus.
- A **traditional database** is a centralised system where data is stored and managed by a single authority (e.g., a company or organisation). Access and modifications are controlled by administrators.

In a distributed ledger, the data cannot be changed once it has been entered without consensus — this is known as **immutability**.

### 2. How transactions work

**Transaction lifecycle**  
Each time a transaction is made between a sender and a receiver, the proposed transaction is received by a mining node on the network, verified for authenticity, and then included in the next block. Once it is included in the block, the data is pushed to the rest of the network, and the recipient receives the transaction.

**Blocks and how they are linked (hashing)**  
Hashing refers to taking any input data and converting it into an alphanumeric coded output of a fixed length. Hashed data cannot be decrypted back to its original form — it is a one-way cryptographic function.

Hashing is fundamental to blockchain technology because the hashing algorithm is used to generate new blocks of data through the mining process (particularly in the PoW algorithm).

**Merkle trees (high-level understanding)**  
A Merkle Tree (also called a hash tree) is a data structure used to verify the contents of large datasets efficiently.

Merkle Trees generate a **Merkle root** by hashing transactions in a block. This allows data validation without downloading the entire blockchain.

At the top of the Merkle tree sits the Merkle root — a single, top-level hash that securely represents all the underlying data. If even a single byte of data at the bottom of the tree changes, the resulting hashes change and produce a different Merkle root. This cascading effect makes the Merkle root a perfect summary of the entire dataset.

Sources: [chain.link](https://chain.link/article/what-is-a-merkle-tree), [Investopedia](https://www.investopedia.com/terms/m/merkle-tree.asp)

### 3. Consensus mechanisms

**Proof of Work (PoW)**  
The original Sybil-resistance algorithm used in blockchain networks (Bitcoin). It requires miners to solve complex mathematical puzzles to validate transactions and create new blocks.

*How PoW works:* Miners compete to solve a cryptographic puzzle. The first miner to solve it gets the right to add a new block to the blockchain. The successful miner is rewarded with newly minted cryptocurrency and transaction fees.

**Proof of Stake (PoS)**  
Instead of relying on computational power, PoS requires validators to hold and “stake” the blockchain’s native cryptocurrency to participate in the consensus process.

Validators are chosen to create a new block based on factors including the size of their stake. They put up a stake as a form of security — behaving maliciously can result in losing some of their holdings. Successful validators are rewarded, but the energy costs are significantly lower than PoW.

**Why consensus is necessary**  
Consensus mechanisms ensure network agreement, trust, and security without human intervention.

The primary benefit is the creation of a **trustless environment**. Consensus also enables censorship resistance (making it difficult for governments or corporations to freeze or reverse transactions) and creates an immutable record of history.

### 4. Key properties

**Decentralisation**  
The distribution of authority and control across a network of participants. No single entity has unilateral control over data or decision-making, eliminating reliance on a central authority like a bank or government.

Decentralised networks rely on nodes — independent participants that collectively verify and approve transactions. Decentralisation is the foundation of blockchain technology, making it resistant to manipulation. By distributing control, users can interact directly, cutting out intermediaries and reducing single points of failure.

**Transparency vs privacy**  
- A **public / transparent blockchain** is available to everyone.
- A **private blockchain** restricts access and is managed by an authority, so it is not necessarily decentralised.

**Security assumptions**  
The main security measures in blockchain are based on cryptography, decentralisation, and consensus, which together ensure trust in transactions. Anonymity also plays a role in public networks (anyone can join).

Private blockchains use identity to confirm membership and access privileges and typically only allow known organisations to join. Consensus is achieved through selective endorsement, where known users verify the transactions.

Source: [IBM](https://www.ibm.com/think/topics/blockchain-security)

---

## Personal notes / reflections

### Architecture based on read, write and commit permissions
*(Diagram reference from course materials)*

### Hash functions
When you input your password into a website, the website hashes it and compares the hash with the hash stored on its database. If it matches, you are logged in (Wilson, 2019).

The Bitcoin network — specifically its Proof of Work algorithm — uses the Secure Hash Algorithm 256 (SHA-256).

**Note on terminology:**  
It is important to distinguish between “cryptocurrency” and “crypto assets”. According to the Intergovernmental Fintech Working Group (IFWG, 2020), a body of South African financial sector regulators, cryptocurrencies are based on decentralised blockchain technology, are electronic in nature, and have the potential to be used in various monetary roles.

However, central banks have steered away from referring to them as cryptocurrencies, as they are deemed neither legal tender nor a form of government-backed currency. Thus, central banks prefer the term **crypto assets**.

### Additional notes on PoS (from Cyfrin Updraft)
Proof-of-Stake can be seen as cutting out the middleman of spending money on hardware. In PoW, spending money on hardware is effectively how you prove you are not multiple entities. PoS takes this idea further and has users directly stake money in the protocol.

**Gasper consensus algorithm**  
A hybrid consensus mechanism used in Ethereum 2.0. It combines Casper FFG (Friendly Finality Gadget) for finality and LMD-GHOST for fork choice. It aims to ensure security, liveness, and energy efficiency in PoS blockchains.

**LMD-GHOST fork choice algorithm**  
Latest Message Driven Greediest Heaviest Observed Sub-Tree. It selects the heaviest chain based on validator votes and prioritises liveness by favouring the most recent messages from validators.

Source: [Cyfrin](https://www.cyfrin.io/blog/blockchain-proof-of-stake-vs-proof-of-work#what-is-proof-of-work-pow)

### Why Consensus Matters: Benefits and Challenges
Achieving consensus at global scale presents significant challenges. Scalability remains a primary hurdle — processing across thousands of nodes can create bottlenecks that limit throughput compared to centralised systems. There is also a risk of centralisation: as mining or staking becomes more professionalised, economies of scale can lead to a small number of entities controlling a large portion of the network’s voting power.

Source: [chain.link](https://chain.link/article/what-is-a-consensus-mechanism)

### How is Decentralisation determined?
Blockchains vary in how decentralised they are. Key factors include:
- **Node count and distribution** — A higher and geographically diverse node count makes it harder for any single entity or region to control the network.
- **Validator count and distribution** — A larger, independent set of validators helps prevent consolidation and collusion during consensus.
- **Token distribution** — A broad spread of token ownership reduces the risk of any one party gaining too much influence over governance or validator operations.
- **Reliance on infrastructure providers** — Minimising dependence on centralised cloud or hosting services protects the network from control by a few large entities.

Source: [Starknet](https://www.starknet.io/glossary/what-is-decentralization-in-blockchain/)

### Issues and Challenges in Blockchain
*(Diagram reference from course materials)*

### Visual of how a Merkle tree works
*(Diagram reference from course materials)*

---

## Resources
- Module 1 Unit 1 (the components of blockchain) – course PDF
- Module 1 Unit 2 (Reaching Consensus) – course PDF
- Bitcoin whitepaper (optional deeper reading)
- Merkle paper (digital signature based on conventional encryption function)
- AJIC article (linked in Notion)
