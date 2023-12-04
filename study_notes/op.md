Optimistic rollups are layer 2 (L2) protocols designed to enhance Ethereum's throughput by offloading computation and state storage off-chain. They process transactions off the main Ethereum chain, providing significant scalability improvements (10-100x) and reduced gas costs for users. Unlike other scaling solutions, optimistic rollups derive security from the Ethereum Mainnet by publishing transaction results on-chain.

Key Features and Components:

1. **Off-Chain Execution:** Optimistic rollups move computation and state storage off-chain, executing transactions outside of Ethereum.

2. **Bundling Transactions:** Operators bundle multiple off-chain transactions into batches before submitting them to Ethereum, spreading fixed costs and reducing fees for users.

3. **Data Availability and Censorship Resistance:** Ethereum Mainnet provides data availability, reducing the risk of malicious acts by rollup operators. It also ensures censorship resistance, preventing operators from censoring users or withholding state data.

4. **Settlement Layer:** Ethereum acts as a settlement layer, providing security, objective finality, and resolution of disputes through fraud proofs.

How Optimistic Rollups Work:

1. **Transaction Execution and Aggregation:** Users submit transactions to operators who aggregate and publish batches on Ethereum.

2. **Submitting Rollup Blocks to Ethereum:** Rollup blocks are compressed and submitted to Ethereum as calldata, reducing gas costs.

3. **State Commitments:** The rollup's state is organized as a Merkle tree, and operators commit to new state roots with each batch.

4. **Fraud Proving:** A fraud-proof scheme allows anyone to challenge the validity of a rollup block, ensuring trustless finality.

5. **L1/L2 Interoperability:** Optimistic rollups support interoperability with Ethereum Mainnet, allowing messages and data to pass between L1 and L2.

Exiting the Rollup:

1. **Withdrawal Process:** Withdrawing from an optimistic rollup to Ethereum involves a challenge period of approximately seven days, ensuring trustless finality.

2. **EVM Compatibility:** Optimistic rollups are compatible with the Ethereum Virtual Machine (EVM), enabling seamless migration of existing smart contracts.

3. **Cross-Chain Contract Calls:** Optimistic rollups facilitate asynchronous contract calls between L1 and L2, supporting interactions between Ethereum contracts and rollup contracts.

Optimistic Rollup Fees:

1. **Gas Fee Scheme:** Similar to Ethereum, optimistic rollups use a gas fee scheme. Fees depend on state writes, calldata size, and L2 operator fees.

2. **Reducing Fees:** Optimistic rollups employ mechanisms such as batching transactions and compressing calldata to reduce fees for users.

Scaling Ethereum:

1. **Data Compression:** Optimistic rollups achieve scalability by compressing transaction data, improving transactions per second (TPS) rates.

2. **Scalability Gains:** Estimates suggest optimistic rollups can achieve processing speeds of around 5,208 transactions per second, offering significant scalability gains.

3. **Data Sharding:** The introduction of data sharding on Ethereum is expected to further enhance scalability for optimistic rollups by increasing blockspace for L2 chains.

Optimistic rollups are layer 2 (L2) protocols for Ethereum that aim to increase the throughput of the Ethereum network by processing transactions off-chain. They achieve this by moving computation and state storage off the main Ethereum chain. The key features and components of optimistic rollups include:

1. **Off-Chain Execution:** Optimistic rollups execute transactions outside of Ethereum, reducing the computational load on the main chain.

2. **Bundling Transactions:** Multiple off-chain transactions are bundled together in batches before being submitted to Ethereum. This allows for the spreading of fixed costs across multiple transactions, reducing fees for end-users.

3. **Data Availability and Censorship Resistance:** Ethereum Mainnet is used for data availability, reducing the risk of malicious acts by rollup operators. It also ensures censorship resistance, preventing operators from censoring users or withholding state data.

4. **Settlement Layer:** Ethereum acts as a settlement layer, providing security, finality, and dispute resolution through fraud proofs.

The process of how optimistic rollups work involves transaction execution and aggregation, submitting rollup blocks to Ethereum, state commitments using Merkle trees, fraud proving, and L1/L2 interoperability. Users can deposit assets into the rollup, and withdrawals involve a challenge period, ensuring trustless finality.

Optimistic rollups use a gas fee scheme similar to Ethereum, where fees depend on state writes, calldata size, and L2 operator fees. Various mechanisms, such as batching transactions and compressing calldata, are employed to reduce fees for users.

In terms of scalability, optimistic rollups achieve significant gains by compressing transaction data, improving transactions per second (TPS) rates. They are estimated to process around 5,208 transactions per second, providing a substantial improvement over the Ethereum base layer.

The introduction of data sharding on Ethereum is expected to further enhance scalability for optimistic rollups by increasing blockspace for L2 chains, using cheaper and impermanent "blob" storage. This is seen as a crucial development to address the limitations imposed by the main Ethereum chain's gas limits. Overall, optimistic rollups offer a promising solution to enhance the scalability and efficiency of the Ethereum network.