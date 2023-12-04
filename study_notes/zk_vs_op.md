There are two main types of rollups used for scaling Ethereum: ZK Rollups (Zero-Knowledge Rollups) and Optimistic Rollups.

1. **ZK Rollups:**
   - **Verification Process:** The batch of transactions is verified for correctness on the Ethereum network using cryptographic validity proofs (zero-knowledge proofs).
   - **Finalization:** After verification passes, the batch of transactions is considered final, similar to any other Ethereum transaction.
   - **Implementation Examples:** zkSync, Loopring, Starknet, Scroll, etc.
   - **Proof Generation:** ZK rollup operators generate proofs of validity for off-chain transactions, such as SNARKs (succinct non-interactive arguments of knowledge).

2. **Optimistic Rollups:**
   - **Verification Process:** There is no mechanism to prove the validity of off-chain transactions upfront. Transactions are considered valid unless proven otherwise.
   - **Finalization:** Transactions are considered "optimistic" and assumed to be valid. If a challenge is submitted, the Optimistic rollup operator must prove the validity of the state and transactions.
   - **Implementation Examples:** Optimism, Arbitrum, etc.
   - **Challenges and Watchers:** Relies on fraud proof systems, and challenges to the submitted state trigger a cumbersome process where the operator must demonstrate the validity of the transactions. Requires watchers to ensure operator honesty.



