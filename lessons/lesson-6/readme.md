# Agnostic Layer 2 Transaction Lifecycle
- L2 components and transaction lifecycle
- L2 rollup process
- L2 examples

![Alt text](/assets/l2_arch.png)
 ## L2 components and transaction lifecycle
  Here's a breakdown of the key components and their roles:

1. **Sequencer or Operator:**
   - **Role:** Acts as a coordinator.
   - **Responsibilities:**
     - Accepts transactions.
     - Passes transactions to a Virtual Machine (VM) for execution.
     - Batches and compresses transactions.
     - Submits the batch of transactions, along with a proof, to the L1.

2. **Virtual Machine (VM):**
   - **Role:** Executes transactions.
   - **Responsibilities:** Processes the transactions received from the sequencer or operator.

3. **L1 Contract:**
   - **Role:** Finalizes the transaction batch and verifies the proof for validity rollups.
   - **Responsibilities:**
     - Receives the transaction batch from the sequencer or operator.
     - Verifies the proof associated with the transaction batch.



## Links shared during the session
- https://rust-lang.github.io/async-book/ 
- https://doc.rust-lang.org/cargo/ 
- https://l2beat.com/scaling/summary#active 
- https://www.lensocr.app/
- https://hashrust.com/blog/arrays-vectors-and-slices-in-rust/ 

