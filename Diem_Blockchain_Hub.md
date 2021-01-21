# Diem Blockchain Hub

A resoucres file for all things related to interacting with Diem Blockchain specifically under use of terminal applications and generalised state purpose activity.

## Contents

*1: Protocol overview*

###### Key concepts of the Diem Blockchain.

* Diem is a blockchain based on distributed ledger technology using the two-tierd approach for designing the transfer of computation across the network of participants.

* Using full nodes and validators sets to authenticate the networks latent execution of valued information between nodes, the have chosen to take a BFT approach to maintaining
consensus between the two sets of authoritze particicpants in the blockchains system. Meaning that 2/3rds of nodes will always have a verified state of the networks whole ledger whos storage holds the most recent state of the Diem blockchain.

* Accounts are able to carry multiple peices of data when stored on the ledgers state. 

* The validators of the network provide API calls from the corresponding connections of full nodes that are operating the party members of Diem's network.

* The transfer of Diem tokens is first validated from a memory pool of pending transactions which validator nodes choose to add as new executed arbitary function calls and state changes to the Diem ledger.

*2: Diem nodes*

###### Introduction to validator and full nodes.

* A Diem node is a peer entity of the Diem ecosystem that tracks the state of the Diem Blockchain. Clients interact with the blockchain via Diem nodes. 

* There are two types of nodes:

  Validator Nodes (Validators) FullNodes

* Each Diem node comprises several logical components:

  JSON-RPC service

  Mempool

  Storage

  Consensus (only validators)

  Execution

  State synchronizer

  Virtual machine
  
  ##### Validator Nodes (validators)
  
* Validator nodes use a distributed consensus protocol to validate the transactions submitted by a Diem client. They process these transactions to include them in the Diem        Blockchain’s database, which validators maintain. This means that these nodes always have the current state of the blockchain.

* A validator node is characterized by the following:

  It participates in consensus.
  
  The JSON-RPC Service component is disabled.
  
  It communicates directly with other validators over a hidden network.
  
  It may be configured to store either all the historical data or part of the historical data from the Diem Blockchain.
  
  It uses its State Synchronizer component to “catch up” to the latest state of the blockchain.
  
  ##### Public FullNodes

* A public FullNode is characterized by the following:

  It uses the same software as the validator.
  
  Consensus is disabled.
  
  It connects directly to one or more validators to submit transactions and synchronize to the state of the Diem Blockchain.
  
* Third-party blockchain explorers, wallets, exchanges, and DApps may run a local FullNode to:

  Leverage the JSON-RPC protocol for richer blockchain interactions.
  
  Get a consistent view of the Diem Payment Network.
  
  Avoid rate limitations on read traffic.
  
  Run custom analytics on historical data.
  
  Get notifications about particular on-chain events.

*3: Accounts*

###### Introduction to account creation, keys, addresses and currencies.

*4: Gas*

###### Learn how the Diem payment network uses gas to charge a transaction fee.

*5: Events*

###### Event types and how to query them.

*6: Diem Clients*

###### An overview of Diem clients.


###### *Transactions*

*7: Transaction Types*

###### Overview of creation/minting administration and payments.

*8: Life of a transaction*

###### Follow a transactions from submission to being committed to the Diem Blockchain.

*9: My first transaction* 

###### Create and execute your first Diem transaction.
