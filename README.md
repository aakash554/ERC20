# Custom ERC20 Token Contract

This repository contains a Solidity smart contract for a custom ERC20 token built on top of OpenZeppelin's ERC20 implementation.

## Contract Details

- **Name**: token
- **Symbol**: ETH
- **Solidity Version**: 0.8.7
- **License**: MIT

## Features

1. **Minting**: Allows the owner to create new tokens.
2. **Burning**: Enables token holders to destroy their tokens.
3. **Transfer**: Permits token holders to transfer tokens to other addresses.
4. **Owner-only functions**: Certain functions are restricted to the contract owner.

## Functions

### Constructor
Initializes the token with the name "Ether" and symbol "ETH". Mints 100 tokens to the contract deployer.
```solidity
constructor() ERC20("Ether", "ETH")
```
### Mint
Allows the owner to mint new tokens and assign them to a specified address.
```solidity
function mint(address receiver, uint256 amount) public payable checking
```

### Burn
Allows any token holder to burn (destroy) a specified amount of their tokens.
```solidity
function burn(uint256 amount) public
```

### Transfer
Overrides the standard ERC20 transfer function with additional checks.
```solidity
function transfer(address receiver, uint256 amount) public virtual override returns (bool)
```

## Dependencies

This contract imports OpenZeppelin's ERC20 implementation:
```solidity
import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/v4.0.0/contracts/token/ERC20/ERC20.sol";
```

## Usage
1. Deploy the contract to an Ethereum network.
2. The deploying address becomes the owner and receives 100 initial tokens.
3. Use the provided functions to mint, burn, and transfer tokens.

## Notes
1. Only the owner can mint new tokens.
2. Any token holder can burn their own tokens.
3. The transfer function includes additional checks for valid addresses and non-zero amounts.

## Authors

Contributors names and contact info

Aakash Sharma  
(aakasharma5504@gmail.com)
