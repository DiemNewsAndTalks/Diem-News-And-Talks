# Diem Blockchain Hub

A resoucres file for all things related to interacting with Diem Blockchain specifically under use of terminal applications and generalised state purpose activity.

## Contents

#### *1: Protocol overview*

###### Key concepts of the Diem Blockchain.

* Diem is a blockchain based on distributed ledger technology using the two-tierd approach for designing the transfer of computation across the network of participants.

* Using full nodes and validators sets to authenticate the networks latent execution of valued information between nodes, the have chosen to take a BFT approach to maintaining
consensus between the two sets of authoritze particicpants in the blockchains system. Meaning that 2/3rds of nodes will always have a verified state of the networks whole ledger whos storage holds the most recent state of the Diem blockchain.

* Accounts are able to carry multiple peices of data when stored on the ledgers state. 

* The validators of the network provide API calls from the corresponding connections of full nodes that are operating the party members of Diem's network.

* The transfer of Diem tokens is first validated from a memory pool of pending transactions which validator nodes choose to add as new executed arbitary function calls and state changes to the Diem ledger.

#### *2: Diem nodes*

###### Introduction to validator and full nodes.

* A Diem node is a peer entity of the Diem ecosystem that tracks the state of the Diem Blockchain. Clients interact with the blockchain via Diem nodes. 

* There are two types of nodes:

  1. Validator Nodes (Validators) - Validator nodes collect transactions and bunch them together then add to the Diem ledgers state altering the last known instance to a more recent update that has allowed new transactions to pass through the network. The validator nodes essentially operate the network to validate a new state of the ledger each time an update is added from a chosen validator. Updates are given 'per block' and are usually around 2mb of data each new term. Validators run the Diem software with consensus enabled to run the BFT algorithm and compete with other nodes on the network in a asynchronous fashion to be able to update the ledgers state. 
  
  2. FullNodes - Full nodes are the body of the network in the Diem world. Connected to eachother, each full node stores a complete state of the entire ledger which is made up of accounts, transactions, scripts and general computing components. Operating as a whole network in unison the behaviour of full nodes requires that they talk to each other and distribute data accordingly to the updates that are being made from the validators. The networks bandwidth is not determined from the full nodes rather the validators ability to  be able to add new abritary sets of data to the ledger. After each new instance that gets added to the ledger, the full nodes that are connected to the validators will pick up the new data and sync themselves accordingly with the new data and then distribute amoung the nearest other participants to update the whole networks state. Full nodes allow for service providers and hosted applications to run a instance of the Diem blockchain, giving the networks users a more efficient and effective interaction with the ledger while allowing them to become a part of maintaining the legitimacy of the network.

* Each Diem node comprises several logical components:

  1. JSON-RPC service - As logic is passed to and from the nodes on the network to other operating clients, the JSON RPC fundamentally allows for the connections between the ledger and the consumers to be able authorized and legitimate. Giving each full node on the network a way to ineract with another, the procedures of the Diem protocol are followed from the rules defined by the RPC and Diem codebase. 

  2. Mempool - The mempool is a list of transactions that have not be added to the ledger. As one wallet sends a transaction, the data that is sent to the network is added to the mempool where it waits to be collected from a validator node. Each transaction that is sent to the mempool has a gas percentage or fee that is sent with the inital value being transacted. The gas percentage or fee determines how long a transaction will be stored in the mempool, transactions with a higher fee will be processed quicker from the validator nodes as the price of execution is more compared to a transaction with a low gas fee. Validator nodes use the mempool to add transactions to the ledger and update the networks state (transactions can not be added to ledger without passing through the mempool).  

  3. Storage - Every node has a store component, this storage component allows each node to validate the prerequisite information to validate the networks state.

  4. Consensus (only validators) - This is the BFT algorthim which will require the validator node to run computation that allows them to accumalate transactions and pack them into blocks to add to the ledger, each validator plays a part in keeping the network secure and compliant with protocol specs.

  5. Execution - ??

  6. State synchronizer - Allows each node on the network to update thier instance of the ledger each time there is a interaction with the node. This may be when the node is turned online, the node is disconnected from the network, when there is updates incoming from validator nodes.

  7. Virtual machine - The virtual machine allows nodes to run computation and execute the functions of applications that are deployed on the blockchain. Each node has a virutal machine to allow computation to flow though the network. 
  
  ##### Validator Nodes (validators)
  
* Validator nodes use a distributed consensus protocol to validate the transactions submitted by a Diem client. They process these transactions to include them in the Diem        Blockchain’s database, which validators maintain. This means that these nodes always have the current state of the blockchain.

* A validator node is characterized by the following:

  1. It participates in consensus. - Allowing each validator node on the network to be able to participate in the consensus activities which in return drives the valiation of the networks state. Each node runs the consensus algorithm that is proposed by the Diem protocol and acts a single entity in the process of validating the network.
  
  2. The JSON-RPC Service component is disabled. - Validator nodes only work the network to validate the transaction input to the ledger. RPC calls can only come from full nodes because of the interaction with client services which only needs to check the state of the ledger and not change any data that is stored on the Diem blockchain.
  
  3. It communicates directly with other validators over a hidden network. - The validators network is a private group of permissioned nodes that operate as governors of the ledger maintaining the legitmacy of transactions that are being added to the blockchain.
  
  4. It may be configured to store either all the historical data or part of the historical data from the Diem Blockchain. - This is due to the set-up by which the validator chooses to pre-configure the settings of thier node which will carry either the whole ledger or just individual sections.
  
  5. It uses its State Synchronizer component to “catch up” to the latest state of the blockchain. - If a validator node is turned off for a while, the state synchronizer will act as a recall component to allow the node to sync up to date with the othe participants on the network. 
  
  ##### Public FullNodes

* A public FullNode is characterized by the following:

  1. It uses the same software as the validator. - Every node that operates aa a sole part of the Diem blockchain's network has to run the Diem software.
  
  2. Consensus is disabled. - Only validator nodes run the consensus component to participate in validating the networks state.
 
  3. It connects directly to one or more validators to submit transactions and synchronize to the state of the Diem Blockchain. - Each node on the network connects to a certain validator usually the closest or most efficent option. When a transaction is sent to mempool from a servicing node the transaction is synchronized on the network before it is mined to the blockchain allowing the validators to authenticate the output of the transaction before updating the state of the ledger.
  
* Third-party blockchain explorers, wallets, exchanges, and DApps may run a local FullNode to:

  1. Leverage the JSON-RPC protocol for richer blockchain interactions.
  
  2. Get a consistent view of the Diem Payment Network.
  
  3. Avoid rate limitations on read traffic.
  
  4. Run custom analytics on historical data.
  
  5. Get notifications about particular on-chain events.

*3: Accounts*

###### Introduction to account creation, keys, addresses and currencies.

* Accounts on the Diem blockchain are 16 bytes and come with 2 resources. RoleId and Account, the role id is the data which grants access of control to the corresponding key and the account is made up from the events handles, authorization key (private key) and the sequence number for the public key. Accounts are created on the DPN (Diem payments network) and are supportive of the designated dealer accounts and regulted virutal asset service providers (VASPS). 

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
