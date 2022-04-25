# Dapp Development Process
Demo projects to get an overview of dApp development, truffle commands and ethereum


## Setup Local Environment
  - Follow the steps from this [link](https://medium.com/interfacing-with-a-blockchain/how-to-set-up-your-ethereum-development-environment-for-macos-cac42af966fd).


## Smart Contract
In this tutorial we are trying to design a smart contract which helps to register voters, allow them to vote for the available proposal and then identify the winning proposals.
##### Resources available : Chairperson(who deploys the smart contract) and Proposals available to vote.

> Ballot - Smart Contract

```
// name of the smart contract
Ballot
// Data
struct Voter {
 uint weight;
 bool Voted;
 uint8 vote;
} Voter;
address chairperson;
mapping(address => Voter) voters;
proposal[]
// Modifiers
modifier onlyOwner 
// Operations
function Ballot() // constructor
function register(..) onlyOwner
function vote(..)

```

## Steps to Develop a Dapp

- [x] Create a directory ; initialize for various components of the dapp using "**truffle init**"
- [x] Create the contracts .sol files in the contracts directory. Compile using "**truffle compile**"
- [x] Generate the test blockchain accounts using "**truffle develop**"
- [x] Deploy the compiled contracts to test blockchain "**truffle migrate**"
- [ ] Add the test files for testing the functions of the contracts "**truffle test**"





