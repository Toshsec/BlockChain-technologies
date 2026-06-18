**Lab:** Lab 1 - Foundations of Blockchain  
**Network Used:** Sepolia Testnet  
## Lab Overview

In this lab, I learned the basic foundations of blockchain technology by completing two activities.

First, I ran a Python blockchain simulation to understand how blocks are linked together using hashes. Then, I deployed and interacted with a simple voting smart contract on the Sepolia Ethereum testnet using Remix and MetaMask.

This lab demonstrated blockchain concepts such as hashing, block linking, immutability, smart contracts, gas fees, wallets, testnets, and public blockchain verification.

---

## Part A: Python Blockchain Simulation

### Objective

The objective of Part A was to simulate a basic blockchain using Python and observe how each block depends on the previous block's hash.

### File Used

simple_blockchain.py
What I Did
I ran the Python file using the following command:
python simple_blockchain.py
The program created a blockchain with multiple blocks. Each block contained data, a timestamp, a previous hash, and its own hash.
After the blockchain was created, the program checked whether the chain was valid. Then, one block was changed to simulate tampering.
Output Observed
Blockchain valid? True
After tampering:
Blockchain valid? False
Explanation
The blockchain was valid at first because every block correctly pointed to the hash of the previous block.
After one block was changed, the blockchain became invalid. This happened because the block's data changed, which caused its hash to change. Since later blocks depend on previous hashes, the chain no longer matched.
This shows the concept of immutability in blockchain. In real blockchains, changing past data is very difficult because it would require changing all following blocks and convincing the network to accept the changed version.
Part B: Deploying a Smart Contract on Sepolia
Objective
The objective of Part B was to deploy and interact with a simple voting smart contract on a live Ethereum testnet.
**Tools Used**: 
Remix IDE
Solidity
MetaMask
Sepolia Testnet
Sepolia Faucet
Sepolia Etherscan
File Used
SimplePoll.sol
Smart Contract Description
The smart contract allowed a user to create a poll with a question and answer options. Users could then vote for one of the options and read the results from the blockchain.
The contract included three main functions:
createPoll
vote
getPoll
Steps Completed
I opened Remix IDE and created a new Solidity file named:
SimplePoll.sol
I compiled the contract using a Solidity compiler version compatible with:
pragma solidity ^0.8.0;
Then I connected Remix to MetaMask using the Browser Extension environment.
I switched MetaMask to the Sepolia testnet and used Sepolia test ETH to pay for gas fees.
After that, I deployed the smart contract and confirmed the transaction in MetaMask.
Poll Interaction
After deploying the contract, I created a poll with the following question:
Should we adopt blockchain in our campus?
The poll options were:
Yes
No
I voted once for:
Yes
Then I voted once for:
No
Finally, I used the getPoll function to read the results.
Results
Question: Should we adopt blockchain in our campus?
Options: Yes, No
Votes: 1, 1
Contract Verification
I verified the deployed contract and transactions using Sepolia Etherscan.
Contract Address
PASTE_YOUR_CONTRACT_ADDRESS_HERE
Sepolia Etherscan Link
https://sepolia.etherscan.io/address/PASTE_YOUR_CONTRACT_ADDRESS_HERE
On Etherscan, I was able to view the contract address, transaction hashes, block confirmations, and gas usage.
Concepts Learned
Hashing
A hash is a unique digital fingerprint of data. In the Python blockchain simulation, each block had a hash that depended on the block's contents.
Previous Hash
Each block stored the hash of the previous block. This linked the blocks together and created a chain.
Immutability
Immutability means that data cannot be changed secretly. If a block is changed, the hash changes and the blockchain becomes invalid.
Smart Contracts
A smart contract is a program stored on the blockchain. The SimplePoll contract allowed users to create a poll, vote, and view results.
Gas Fees
Gas fees are paid to process transactions on the blockchain. In this lab, Sepolia test ETH was used to pay gas fees.
Testnet
A testnet is a blockchain network used for practice and testing. Sepolia allowed me to deploy and test the contract without using real ETH.
Blockchain Explorer
A blockchain explorer like Sepolia Etherscan allows anyone to view public blockchain transactions, contract addresses, gas usage, and confirmations.
Conclusion
In this lab, I learned how blockchain works at a basic level by first simulating a blockchain in Python and then deploying a smart contract on the Sepolia Ethereum testnet.
The Python simulation showed how blocks are linked by hashes and how changing one block can break the chain. The Solidity smart contract showed how blockchain can be used to store and manage voting data on a public decentralized network.
This lab helped me understand blockchain immutability, smart contracts, wallets, gas fees, and public transaction verification.
