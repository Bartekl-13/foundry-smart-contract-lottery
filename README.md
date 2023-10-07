# Proveably Random Raffle Contract

## About

This repository is to create a provably random smart contract lottery.

### What's it functionality?

Users can enter the raffle by calling `enterRaffle()` function to pay `entranceFee`.

The user will be able to claim their prize if they win, or keep all of their money in case they lose (if there are no more other players in the lottery).

After some amount of time the winner will be programatically chosen using Chainlink Automation automatically calling to Chainlink VRF node in order to provide a verifiably random number.

## Testing

Right now, unit tests for Raffle contract itself are provided. However, in the future tests for `Interactions.s.sol` and dployment scripts will be added.

### On local node

In order to run a test on your local anvil node, run:

```shell
$ forge test
```

### On Sepolia testnet

In order to run a test on sepolia testnet, first change `.envexample` file to `.env` and include your private key, API and rpc url. Then run:

```shell
$ source .env
$ forge test --fork-url $SEPOLIA_RPC_URL
```
