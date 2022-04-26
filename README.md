# Dapp Development Process
Demo projects to get an overview of dApp development, truffle commands and ethereum


## Setup Local Environment
  - Follow the steps from this [link](https://medium.com/interfacing-with-a-blockchain/how-to-set-up-your-ethereum-development-environment-for-macos-cac42af966fd).
  - Solidity version 0.8.13


## DEMO 1 - Ballot1 
This demo will help to understand the basic structure of a dapp without any user interface and web3 wallet connectivity.

### Smart Contract
In this tutorial we are trying to design a smart contract which helps to register voters, allow them to vote for the available proposal and then identify the winning proposals.
##### Resources available : Chairperson(who deploys the smart contract) and Proposals available to vote.

> Ballot - Smart Contract

Name of the smart contract
```
Ballot
```
Data
```
struct Voter {
 uint weight;
 bool Voted;
 uint8 vote;
} Voter;
address chairperson;
mapping(address => Voter) voters;
proposal[]
```
Modifiers
```
modifier onlyOwner 
```
Operations
```
function Ballot() // constructor
function register(..) onlyOwner
function vote(..)
```

### Commands to be followed in this demo

- [x] Create a directory ; initialize for various components of the dapp using "**truffle init**"
- [x] Create the contracts .sol files in the contracts directory. Compile using "**truffle compile**"
- [x] Generate the test blockchain accounts using "**truffle develop**"
- [x] Deploy the compiled contracts to test blockchain "**truffle migrate**"
- [x] Add the test files for testing the functions of the contracts "**truffle test**"


#### truffle init
It will create some folders and file.
- contracts
  - It contains an important contract called _migration.sol_, smart contract for facilitating deployment.
  - We will create the Ballot.sol smart contract for this tutorial as well and place inside this folder.
- migrations
  - Truffle used a migration system to handle contract deployments, hence this folder contains a special smart contract that is used to keep track of changes.
- test
  - This directory contains both Javascript and Solidity tests for our smart contracts.
- truffle-config.js
  - This is a configuration file which contains truffle development configuration information that specify blockchain network ID, IP and RPC port.

#### truffle compile
Any compilation errors can be seen during this process and after a successful compilation it will generate some artifacts which can be seen in the folder **_build/contracts_**

#### truffle develop
- Before running this command, make sure to configure the network_id and other parameters based on the environment (development/production) in _truffle-config.js_ file.
- After running this command, it will create accounts on the test chain and also some seed words (refer the folder **_seed_words/truffle_develop.txt_**)
- Also save the seed words and account names to use it through Management APIs (like getBalance) in the truffle console which also opens up after running truffle develop.

#### truffle migrate --reset
- This command wil migrate the deployed contracts into the test chain and ready to use to initiate the transactions
- Since we are running command on development environment, we can always use --reset to start transactions from the begining and refresh the smart contracts. But in production environment, _once a smart contract is deployed we can't change or reset it_.


#### truffle test
- This will run all the tests written in test.js
- before running this command, make sure to run truffle develop