# Token-Based Lottery DApp

A secure and decentralized lottery system implemented in Solidity that enables token-based participation with built-in security controls and automated winner selection.

## Core Features

- Whitelisted participation system
- One-entry-per-user limit
- Time-bounded lottery rounds
- Automated winner selection
- Secure reward distribution
- ERC20 token integration

## Smart Contracts

### Main Contracts
- `TokenLottery.sol`: Core lottery implementation
- `IERC20.sol`: ERC20 token interface
- `Token.sol`: Sample token implementation

## Setup Instructions

### Prerequisites

```bash
# Install required dependencies
npm install --save-dev hardhat
npm install @openzeppelin/contracts
```

### Installation

```bash
git clone <repository_url>
cd <repository_directory>
npm install
```

### Deployment Steps

1. Compile contracts:
```bash
npx hardhat compile
```

2. Deploy to network:
```bash
npx hardhat run scripts/deploy.js --network <network_name>
```

## Contract Interface

### Administrative Functions
- `whitelist(address _user)`: Add participants to whitelist
- `removeFromWhitelist(address _user)`: Remove participants from whitelist

### User Functions
- `enterLottery(uint256 _amount)`: Enter lottery with tokens
- `getWinner()`: Retrieve current winner

### System Functions
- `endLottery()`: Conclude current lottery round

## Events
- `Entered(address indexed user, uint256 amount)`
- `WinnerSelected(address indexed winner, uint256 reward)`

## Security Features

- OpenZeppelin secure token handling
- Role-based access control
- Rate limiting mechanisms
- Anti-reentrancy protection
- Time-locked operations

## Development Commands

```bash
npx hardhat help
npx hardhat test
REPORT_GAS=true npx hardhat test
npx hardhat node
```

## Security Notice

This contract requires proper security audit before production deployment. Use at your own risk.
