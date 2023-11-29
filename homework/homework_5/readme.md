## Homework 5
------------------------------------------------
Listen to Zero Knowledge podcast episode 151 comparing Optimistic and
zkRollups

****Episode 151: John Adler on Optimistic vs ZK Rollup and the data availability problem****

John Adler – co-founder of Lazy Ledger (now Celestia) and Fuel Labs

### Simplified definition

> Optimistic Rollups are similar to ZK Rollups, but instead of using validity proofs, they use fraud proofs.
> 
- A fraud proof proves that something is **invalid**.
- A validity proof proves that something is **valid**.
- With a fraud proof, you make a claim and wait for a period of time to see if a fraud proof is presented. If no fraud proof is presented within that time, you assume it's valid.
- `Someone watching needs to create the fraud proof.`
- `Both plasma and channels utilize fraud proofs.`
    - **Channels** have limited participation and liquidity constraints. In order to receive a payment, something like, inbound liquidity, is required.
    - **Plasma** is permissioned” because of the data availability problem “ and allows for arbitrary smart contracts. This is possible because plasma does not rely on general-purpose fraud proofs. Instead, it utilizes an exit game based on owned assets.
        - The original plasma paper described the possibility of running smart contracts, but it didn't provide a concrete system implementation. It mainly presented a high-level abstract idea of how plasma could enable smart contract execution.
        - All the implementations focus solely on payment and do not address the potential of general-purpose smart contracts.
- Optimistic rollups:
    - Open participation like plasma, unlike channels.
    - No liquidity constraints like channels.
    - Permissionless and use general-purpose fraud proofs, enabling potential execution of any smart contract.
- How to transfer value off-chain, such as 10 ETH, without the need to lock up this value in a channel?
    - `The off chain has to be a blockchain`
- Trustless and  permissionless  in plasma and rollups:
    - Permissionless means that you don't have to ask for permission.
    - Permissioned means that if you have a single operator "on a plasma",
    - Permissionless: anyone can make a state transition, anyone can be a block producer, and anyone can force a state transition.
    - State safety vs. state liveliness:
        - State liveliness means that you consume your state within a finite time.
        - State safety means that no one can consume your state without your authorization.
        
        So, state liveliness allows you to move your coins, and state safety ensures that no one can move your coins.
        
    
    We observe that if a system has both state liveliness and state safety, it is trustless. As long as you can keep moving your coins and no one can steal them, you don't have to trust the people who run the system. To address your question, plasma is permissioned, but it can still be trustless. the problem that it'd be in permission is that **the operator can force people to go back to the main chain.**
    
    Increasing the size of history is not a problem because history is write once, never read, unlike state. Therefore, there is no need to keep all the history on every full node. Once you have the current state of the system, you can discard the history. Moving information from Layer 1's state to its history makes it more sustainable and cost-effective.



    ****Podcast Summary: John Adler on Optimistic vs ZK Rollup and the Data Availability Problem****

**Episode 151: Key Points**

1. **Optimistic Rollups vs. ZK Rollups:**
    - **Optimistic Rollups:** Use fraud proofs to determine if a transaction is invalid. If no fraud proof is presented within a set period, the transaction is assumed valid.
    - **ZK Rollups:** Rely on validity proofs to confirm the validity of transactions. These proofs provide cryptographic evidence that the transaction is correct.
    - **Fraud Proofs:** Prove invalidity, requiring someone to create a fraud proof within a time frame.
    - **Validity Proofs:** Prove validity cryptographically, ensuring the correctness of a transaction.

2. **Channel and Plasma Overview:**
    - **Channels:** Have limited participation and liquidity constraints. They require inbound liquidity for transactions.
    - **Plasma:** Utilizes permissioned exits based on owned assets. It allows for arbitrary smart contracts but faces data availability issues.

3. **Optimistic Rollups Characteristics:**
    - Open participation and no liquidity constraints, similar to plasma.
    - Permissionless and use general-purpose fraud proofs, allowing potential execution of any smart contract.

4. **Transfer Value Off-Chain:**
    - To transfer value off-chain without locking up funds, the off-chain solution needs to be a blockchain.

5. **Trustless and Permissionless:**
    - Trustless: No need to trust individuals running the system.
    - Permissionless: Anyone can make state transitions and be a block producer.

6. **State Safety vs. State Liveliness:**
    - **State Liveliness:** Consuming state within a finite time.
    - **State Safety:** Ensuring no one can consume state without authorization.

7. **Lazy Ledger (Celestia):**
    - Provides a solution to the data availability problem.
    - Uses erasure coding to ensure data availability with sublinear costs.
    - Lazy Ledger is a blockchain that focuses solely on data availability.

8. **Sharding and Data Availability:**
    - Sharding aims to increase data availability throughput.
    - Lazy Ledger and similar solutions focus on providing shared data availability for various blockchains.

9. **Serenity (ETH2) Proposal:**
    - Serenity aims for rollup-centric focus rather than traditional sharding execution.
    - Rollups could run on Ethereum, acting as shards, providing domain-specific optimizations.

10. **Data Availability Challenges and Solutions:**
    - Data availability and ordering are critical for blockchain functionality.
    - Lazy Ledger addresses data availability challenges using erasure coding.
    - Overhead in Serenity's sharded data availability design might limit its effectiveness.

11. **Namespace Merkle Tree (Lazy Ledger):**
    - Lazy Ledger uses a Namespace Merkle Tree optimization.
    - Each application defines its Namespace space, allowing efficient extraction of application-specific data.

12. **Application in L2 Contexts:**
    - Lazy Ledger can be utilized in Layer 2 contexts, supporting rollups and sidechains.
    - Provides a shared data availability layer for multiple blockchains.

13. **Throughput Considerations:**
    - Systems focusing solely on data availability can achieve higher throughput.
    - Sharded execution might reduce throughput compared to prioritizing data availability.

14. **Comparison with Polkadot:**
    - Similarities between Lazy Ledger and sharded blockchains like Polkadot.
    - Both aim to solve data availability challenges and increase throughput.

15. **Beacon Chain (ETH2):**
    - Beacon Chain focuses on shuffling the validator set but doesn't directly address sharded data availability.

16. **Sustainability and Cost-Effectiveness:**
    - Lazy Ledger's approach of moving information from Layer 1's state to history increases sustainability and reduces costs.

17. **Conclusion:**
    - The podcast covers Optimistic vs. ZK Rollups, data availability challenges, and innovative solutions like Lazy Ledger.

*Note: The summary provides key points from the podcast, and explanations are included where necessary for clarity.*