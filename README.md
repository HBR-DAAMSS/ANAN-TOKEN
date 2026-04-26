# ANAN-TOKEN
ANAN is a fixed-supply BEP20 token deployed on Binance Smart Chain (BSC).
# ANAN Token (BEP20)

ANAN is a fixed-supply BEP20 token deployed on Binance Smart Chain (BSC).

## Token Information
Name: ANAN  
Symbol: ANAN  
Total Supply: 1,000,000  
Decimals: 18  
Network: Binance Smart Chain (BSC)  
License: MIT  
Minting: Disabled  
Burning: Disabled  

## Features
- Fixed supply (minted once at deployment)
- No mint function
- No burn function
- Fully ERC20 / BEP20 compatible
- Built using OpenZeppelin standard

## Smart Contract

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract ANAN is ERC20 {

    uint256 private constant INITIAL_SUPPLY = 1_000_000 * 10**18;

    constructor() ERC20("ANAN", "ANAN") {
        _mint(msg.sender, INITIAL_SUPPLY);
    }
}
