# MaterialToken Smart Contract 

## Overview

The MaterialToken smart contract is an Ethereum-based ERC-20 token that represents a virtual currency used for the creation and destruction of virtual objects. Each object is associated with a specific cost in MaterialToken (MTK), and users can redeem these objects by burning the corresponding amount of tokens.

The smart contract is built using the Solidity programming language and utilizes the OpenZeppelin library for ERC-20 implementation and additional features. The contract includes functionalities for minting, burning, transferring tokens, and redeeming objects.

## Functionality

### ERC-20 Token

The MaterialToken contract is an ERC-20 token, which means it adheres to the ERC-20 standard for fungible tokens on the Ethereum blockchain. Users can transfer, mint, and burn tokens.

### Minting

The owner of the contract can mint new MaterialToken tokens and distribute them to specified addresses. This functionality is restricted to the contract owner for maintaining control over token creation.

```solidity
function mint(address to, uint256 numTokens) external onlyOwner
```

### Burning

Users can burn their MaterialToken tokens, reducing the total supply. This is typically done when redeeming virtual objects or as a mechanism for removing tokens from circulation.

```solidity
function burn(uint256 numTokens) external
```

### Object Redemption

Users can redeem virtual objects by burning a specific amount of MaterialToken tokens. The type of object is determined by an enumeration called `Object`, and each object has a different associated cost in tokens.

```solidity
function redeemObject(uint8 objectNumber) external
```

### Object Transfer

Users can transfer MaterialToken tokens to other addresses, facilitating the exchange of tokens between participants.

```solidity
function transfer_(address recipient, uint256 numTokens) external
```

### Ownership

The contract includes the Ownable contract from OpenZeppelin, ensuring that certain functions, such as minting, are only accessible to the owner of the contract.

## Objects and Costs

The virtual objects that users can redeem are categorized as Cloth, Wood, Metal, and Leather. Each object has a predefined cost in MaterialToken tokens:

- Cloth: 750 tokens
- Wood: 500 tokens
- Metal: 1000 tokens
- Leather: 1200 tokens

## Events

The contract emits an event, `ObjectRedeemed`, whenever a user successfully redeems a virtual object. The event includes information about the user, the redeemed object, and the associated token cost.

## Usage

Developers and users can interact with the MaterialToken smart contract using Ethereum wallets, smart contract interfaces, or by integrating it into decentralized applications (DApps) on the Ethereum blockchain.

## Security Considerations

Developers should be cautious when deploying and interacting with smart contracts on the Ethereum blockchain. Proper testing and auditing are recommended to ensure the security and functionality of the MaterialToken contract.

## License

This smart contract is released under the MIT License. See the SPDX-License-Identifier tag in the contract source code for more details.

## Author
Imran khan

imrankhan924738@gmail.com
