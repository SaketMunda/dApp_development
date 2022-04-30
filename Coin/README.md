## Smart Contract

Note : This is in progress

> Coin
To Illustrate event handling and all the operations we will use Coin dapp. (Coin folder)
#### Goal is to create a program where minter can only mint new coins for a given address and transfer coins from one account to another.


### Structure
Same as Ballot2 

### Design

```
address minter;
mapping address => balances
```

```
event sent(from, to, amount)
Coin()
mint(address receiver, unint amt)
transfer(address receiver, unint amt)
```

## Setting up an event

We define an event by its name and parameters.

```
event sent(from, to, amount)
```

## Consume an event


## Handle the event

Following the truffle documentation, we will handle it in javascript app, App.js
> This approach enables us to conveniently handle the events and inject the javascript assets in the web to display the event notification.