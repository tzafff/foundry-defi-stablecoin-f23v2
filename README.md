
# Foundry DeFi Stablecoin

### This project implements a decentralized stablecoin system using Ethereum smart contracts. The stablecoin is designed to be pegged to USD, exogenously collateralized with wETH and wBTC, and algorithmically stabilized.




## Features
1. Stablecoin Pegging:
- Pegged to $1.00 using Chainlink Price Feeds.
- Allows for the exchange of ETH and BTC to maintain the peg.
2. Stability Mechanism:
- Algorithmically controlled minting based on collateral deposits.
- Ensures the system is always over-collateralized.
3. Collateral:
- Accepts wETH and wBTC as collateral.
4. Testing
- Robust testing with unit tests, fuzz testing, and invariant tests using Foundry

## Contracts

1. DSCEngine.sol
- This is the core contract that handles the minting, redeeming of the stablecoin, and managing collateral.

2. DecentralizedStableCoin.sol
- This contract implements the ERC20 token functionality for the stablecoin, including minting and burning capabilities.


## Testing

1. Unit
2. Integration
3. Forked
4. Staging
5. Fuzzing

```shell
forge test
```
### Test Coverage
```shell
forge coverage
```
and for coverage based testing:
```shell
forge coverage --report debug
```

# Deployment to a testnet or mainnet
1. Setup environment variables

You'll want to set your SEPOLIA_RPC_URL and PRIVATE_KEY as environment variables. You can add them to a .env file, similar to what you see in .env.example.

- PRIVATE_KEY: The private key of your account (like from metamask). NOTE: FOR DEVELOPMENT, PLEASE USE A KEY THAT DOESN'T HAVE ANY REAL FUNDS ASSOCIATED WITH IT.
You can learn how to export it here.
- SEPOLIA_RPC_URL: This is url of the sepolia testnet node you're working with. You can get setup with one for free from Alchemy
Optionally, add your ETHERSCAN_API_KEY if you want to verify your contract on Etherscan.

1. Get testnet ETH

Head over to faucets.chain.link and get some testnet ETH. You should see the ETH show up in your metamask.

2. Deploy
```shell
make deploy ARGS="--network sepolia"
```



## Build with Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Anvil

```shell
$ anvil
```

# Author
- Christos Tzaferis
