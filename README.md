# Dapp Development Process
Demo projects to get an overview of dApp development, truffle commands and ethereum


## Setup Local Environment
  - Follow the steps from this [link](https://medium.com/interfacing-with-a-blockchain/how-to-set-up-your-ethereum-development-environment-for-macos-cac42af966fd).
  - Solidity version 0.8.13


## DEMO 1 - Ballot1 
This demo will help to understand the basic structure of a dapp without any user interface and web3 wallet connectivity. Understand the basic truffle commands.

### Truffle Commands

- [x] Create a directory ; initialize for various components of the dapp using "**truffle init**"
- [x] Create the contracts .sol files in the contracts directory. Compile using "**truffle compile**"
- [x] Generate the test blockchain accounts using "**truffle develop**"
- [x] Deploy the compiled contracts to test blockchain "**truffle migrate**"
- [x] Add the test files for testing the functions of the contracts "**truffle test**"

## DEMO 2 - Ballot2 
This demo will help to understand dapp development with the integration of user interface front-end to the smart contracts, and blockchain back-end.

## DEMO 3 - Coin
This demo will help to understand dapp development with event handling.

### Events are useful for :
- Pushing Notification
- Logging activities
- Asynchronous operations between sender and reciever
- Efficient alternative for polling