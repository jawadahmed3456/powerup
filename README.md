# PowerUpToken 

## Overview

The PowerUpToken smart contract is an Ethereum-based ERC-20 token that extends the functionality of standard ERC-20 tokens by incorporating features such as burning, pausing, and power-up redemption. This contract is designed to represent a fungible token that users can transfer, burn, and redeem for various in-game "power-ups."

## Features

### ERC-20 Standard Compliance

The PowerUpToken contract follows the ERC-20 standard, providing basic token functionalities such as transferring tokens between addresses.

### Ownable

The contract includes the Ownable module, allowing the owner (deployer) to execute specific privileged functions like minting new tokens.

### ERC-20 Burnable

Users can burn (destroy) a specified number of tokens, reducing their token balance.

### Pausable

The contract can be paused and unpaused by the owner. When paused, certain functions like power-up redemption and token transfers are disabled, adding an extra layer of security.

### Power-Up Redemption

Users can redeem specific in-game "power-ups" by burning a certain amount of tokens. Power-ups include "Health Boost," "Speed Boost," "Strength Boost," and "Invisibility." Each power-up has an associated cost in tokens, and users must have a sufficient token balance to redeem a power-up.

### Events

The contract emits various events, including `PowerUpRedeemed`, `PowerUpBalanceChecked`, `TotalSupplyChecked`, `TokenSymbolChecked`, `TokenPaused`, `TokenUnpaused`, and `TokensTransferred`. These events can be used to track important activities on the blockchain.

## Functions

- `mint_tokens`: Allows the owner to mint new tokens and allocate them to a specific address.

- `burn_tokens`: Enables users to burn a specified number of tokens, reducing their token balance.

- `redeemPowerUp`: Allows users to redeem specific power-ups by burning the required amount of tokens.

- `checkPowerUpBalance`: Allows checking the balance of tokens for a specific power-up and address.

- `checkTotalSupply`: Provides the total supply of PowerUpToken.

- `checkTokenSymbol`: Returns the symbol of the token ("PUT").

- `pauseToken` and `unpauseToken`: Allows the owner to pause and unpause the contract, respectively.

- `transferTokens`: Enables users to transfer tokens to another address.

## Deployment

The contract is deployed with initial power-up costs for each type. The default power-ups are "Health Boost," "Speed Boost," "Strength Boost," and "Invisibility." The owner can modify the power-up costs and other parameters by updating the contract.

## Usage

Developers can integrate the PowerUpToken contract into their decentralized applications (dApps) to implement fungible tokens with additional features such as burning and power-up redemption.

## License

This smart contract is released under the MIT License. See the SPDX-License-Identifier in the source code for more details.
