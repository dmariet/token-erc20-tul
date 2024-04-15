# token-erc20-tul

## Overview
The Token contract is an ERC20 token implementation that includes access control functionality provided by the OpenZeppelin AccessControl library.

## Features
- Implements the ERC20 standard for fungible tokens.
- Provides access control functionality for minting new tokens.
- Token name: Tulsa Token
- Token symbol: TUL
- Token decimals: 2

## Roles
- **DEFAULT_ADMIN_ROLE:** The default admin role that is granted to the deployer of the contract.
- **MINTER_ROLE:** Role required to mint new tokens.

## Functions
### `constructor()`
- Initializes the contract and grants the DEFAULT_ADMIN_ROLE and MINTER_ROLE to the deployer.

### `mint(address to, uint256 amount)`
- Mints a specified amount of tokens and assigns them to the specified address.
- Requires the caller to have the MINTER_ROLE.

### `decimals()`
- Returns the number of decimals used to display the token's value.

## Usage
1. Deploy the Token contract.
2. Use the `mint` function to mint new tokens, specifying the recipient address and the amount.
3. Transfer tokens between addresses using the standard ERC20 transfer functions.
4. Use access control functions to manage roles and permissions as needed.

## Security Considerations
- Ensure that only trusted addresses are granted the MINTER_ROLE to prevent unauthorized token minting.
- Use appropriate access control mechanisms to restrict access to sensitive functions.

## License
This contract is released under the MIT License.
