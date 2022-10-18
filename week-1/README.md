# Blockchain Fundamentals

## Introduction
### What is Blockchain

This is a technology with operates by adopting a distributed ledger to track transactions. The ledger is a series of blocks containing transaction data. It starts out with the genesis block. New blocks are then added to the ledger after their transactions have been verified by the nodes that form the network upon which the blockchain is built. Each block is linked to the block preceeding it to eventually form a giant linked list in a manner of speaking.

The nodes which verify block transactions are called validators and they consists of miner (machines owned by people on the blockchain) which adopt a consensus mechanism in other to perform their validator functions.

### Consensus

There are different types of consensus mechanisms. Two popular ones include:
- Proof of work and 
- Proof of stake

**Proof of Work**:
This consensus mechanism operates by having miners expend energy or compute power in order to perform a rigorous mathematical calculation which involves finding out the hash of a block. This hash once verified by the majority of the validators on the network is assigned as the blocks ID and is used to effect the linking the forms the blockchain. Each block has the hash of the block before it. The algorithm used to calculate the hash is a one way algorithm meaning that the input that gave the hash can not be determined from the hash itself. Also the hash is impossible to fake as even just a little change in the block data that forms the hash would generate a completely different hash in every way unlike the original hash. These features of the ahshing algorithm make it incredibly difficult and almost impossible to fake transactions on the blockchain. 

When miners solve the problem correctly they are incentivized by being added to a pool from which a miner will be selected randomly and rewarded some tokens.

Using the proof of work mechanism a miner can opt to not perform it's validation roles or relinquish their role without any cost to them. This however reduces the security of the chain because the more the miners on the chain the higher the security.

**Proof of Stake**:
This consensus mechanism was essentially implemented as a replacement for proof of work. It offers some solutions to the security issues posed by the proof of Work model. In this method, the validators commit (stake) at least a minimum amount of tokens (32 ETH for ethereum). This commitment then binds them to perform their validator roles. However, if you don't have upto 32 ETH, you can join a validator pool and contribute an ERC-20 token. This will make you eligible for rewards when your validator node is selected.

The validator nodes are selected randomly for verifying block hashes and rewards are proportional to your stake. This method is preferred to proof of work because of its lower energy requirements to becaome a validator. This effectively reduces the energy footprint of the blockchain that adopts this consensus mechanism. It also improves security as more people are encouraged to participate as validators as opposed to the proof of work system where only the elite who could afford heavy duty hardware could participate in the validation process.

The proof of stake mechanism is not without demerits though. There are still possible security risks like the 51% attack. This however, would require the perpertrators to own 51% of the collective staked tokens on the network.

### Layers of the Blockchain
- Layer 0
- Layer 1
- Layer 2
- Layer 3

**Layer 0**:
This consists of the network upon which the blockchain is built. It accounts for the protocols and communication systems between the nodes on the network. Polkadot, Avalanche, Cardano, and Cosmos are some examples of Layer 0 blockchains.

**Layer 1**:
This consist of the actual blockchain. It controls and regulates process such as validation, conflict resolution and adding blocks to the block chain. It also includes the pprogramming languages used to develop on the chain. Ethereum, Binance Smart Chain, Bitcoin, and Solana are all examples of Layer 1.

**Layer 2**:
This layer exists as somewhat of a turbo booster for Layer 1. It provides more nodes for the blockchain effectively increasing it's processing power and security. It exists as an extra network built ontop of the Layer 1 blockchain to abstract some of Layer 1's operations to itself and let Layer 1 focus on adding and validation blocks on the blockchain. An example is the Lighting network built on top of the bitcoin blockchain.

**Layer 3**:
This layer includes platforms which utilizes the blockchain to implement solutions. It is the user facing side of the blockchain. It provides functionalities such as intra and inter blockchain communication. An example of Layer 3 blockchains are Dapps (Decentralized Applications).


<hr>


# Create a local development environment for solidity on ubuntu

## Packages required
- geth
- truffle
- ethereum
- ganache
- nodejs
- npm

## Procedure
### Step 1: Install `Geth`
1 `sudo apt install software-properties-common`
2 `sudo add-apt-repository -y ppa:ethereum/ethereum`
3 `sudo apt update`
4 `sudo apt install ethereum -y`
5 `geth version`

### Step 2: Install `ganache`
1 Goto `https://truffleframework.com/ganache`
2 Download the ganache app image for linux (the site detects your OS automatically)
3 Make app image executable and run it

### Step 3: Install Nodejs and NPM
1 Check if both packages are installed by running `node -v` or `npm -v`
2 Install nodejs if not present
3 Goto `https://nodejs.org/en/download/package-manager`.
4 Select your linux distrubution
5 Make sure `curl` is installed on your system `sudo apt install curl -y`
6 Follow the procedure on the nodejs site.
7 Run `sudo apt install -y nodejs`
8 Verify your installation `node -v` and `npm -v`


### Step 4: Install Truffle 4
1 Goto `https://truffleframwork.com` for installation instructions
2 Uninstall previous versions of truffle 
> ```bash
sudo npm uninstall -g truffle
```
3 Install truffle v4.0.4
> ```bash
sudo npm install truffle@4.0.4 -g
```

### Step 5: Install any text editor of your choice.
- Atom
- Vs Code
- Sublime etc.