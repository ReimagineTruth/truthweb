---
icon: copy
---

# Dual Value System Guide

The Bridge System is a critical component of TruthWeb , enabling seamless cross-chain interoperability between the Pi Network and other blockchain ecosystems. This system allows users to transfer Pi tokens across blockchains, unlocking new opportunities in decentralized finance (DeFi), non-fungible tokens (NFTs), and multi-chain ecosystems.

Below is a comprehensive guide to the Bridge System , including its architecture, functionality, implementation details, and use cases.

Table of Contents Overview How It Works Key Features Implementation Details Use Cases API Reference FAQs OverviewThe Bridge System acts as a secure intermediary that facilitates the transfer of Pi tokens between blockchains. It locks Pi tokens on the source chain, mints equivalent wrapped tokens on the target chain, and ensures a 1:1 peg between the two. This process enables Pi to be used in external ecosystems like Ethereum, Binance Smart Chain, and others.

How It WorksThe Bridge System operates through a series of steps involving smart contracts, decentralized oracles, and token wrapping mechanisms:

Deposit Pi into the Bridge : Users send their Pi tokens to the Bridge System's smart contract. The system locks the deposited Pi tokens securely. Token Wrapping : The Bridge System mints an equivalent amount of wrapped Pi tokens (e.g., wPi) on the target blockchain. These wrapped tokens are compatible with the target chain's ecosystem. Transfer Across Chains : Wrapped Pi tokens are transferred to the user's wallet on the target blockchain. Users can now interact with dApps, DeFi protocols, or NFT marketplaces using wPi. Reverse Process : To convert wrapped Pi tokens back to Pi, users initiate a reverse bridge transfer. The Bridge System burns the wrapped tokens and releases the original Pi tokens from the locked pool. Key FeaturesCross-Chain Interoperability : Enables seamless interaction between Pi Network and other blockchains. Token Wrapping : Converts Pi tokens into wrapped tokens for compatibility with external ecosystems. Decentralized Oracles : Ensures accurate and real-time validation of cross-chain transactions. Security Protocols : Protects against fraud and ensures trustless operations. Scalability : Supports multiple blockchains and future expansions. Implementation DetailsCore Components Smart Contracts : Automate the locking, minting, burning, and releasing of tokens. Example: A Solidity-based smart contract for the Bridge System.&#x20;

```solution-file
// Solidity Smart Contract for Bridge System
pragma solidity ^0.8.0;

contract BridgeSystem {
    address public bridgeAddress;
    uint256 public totalLockedPi;
    mapping(address => uint256) public balances;

    event PiLocked(address indexed user, uint256 amount);
    event PiReleased(address indexed user, uint256 amount);

    constructor() {
        bridgeAddress = msg.sender;
    }

    function lockPi(uint256 amount) external {
        require(amount > 0, "Amount must be greater than zero");
        balances[msg.sender] += amount;
        totalLockedPi += amount;
        emit PiLocked(msg.sender, amount);
    }

    function releasePi(address user, uint256 amount) external {
        require(msg.sender == bridgeAddress, "Only bridge can release Pi");
        require(balances[user] >= amount, "Insufficient balance");
        balances[user] -= amount;
        totalLockedPi -= amount;
        emit PiReleased(user, amount);
    }
}
```

1. **Decentralized Oracles** :
   * Monitor and validate transactions across chains.
   * Example: Using Chainlink or Band Protocol for cross-chain data verification.
2. **Wrapped Tokens** :
   * Represent Pi tokens on external blockchains.
   * Example: wPi (Wrapped Pi) on Ethereum.
3. **API Integration** :
   * APIs connect the frontend (user interface) with the backend (bridge system).
   * Example: An API endpoint to fetch bridge status.

```javascript
app.get('/api/bridge/status', async (req, res) => {
    const bridgeStatus = await fetchBridgeStatus();
    res.json(bridgeStatus);
});
```

1. **Security Measures** :
   * Multi-signature wallets for fund management.
   * Regular audits to ensure smart contract integrity.

***

### **Use Cases** \<a name="use-cases">\</a>

1. **DeFi Participation** :
   * Use wrapped Pi tokens for lending, borrowing, or yield farming on platforms like Aave or Compound.
2. **NFT Trading** :
   * Purchase NFTs on Ethereum or Binance Smart Chain using wrapped Pi tokens.
3. **Cross-Chain Swaps** :
   * Swap Pi for other cryptocurrencies via decentralized exchanges (DEXs).
4. **Staking Rewards** :
   * Stake wrapped Pi tokens to earn rewards in DeFi protocols.
5. **Global Payments** :
   * Send Pi to users on other blockchains for faster and cheaper transactions.

***

### **API Reference** \<a name="api-reference">\</a>

#### **Endpoints**

1. **Deposit Pi into the Bridge**
   * **URL** : `/api/bridge/deposit`
   * **Method** : `POST`
   * **Body** :

```json
{
  "amount": 100,
  "targetChain": "ethereum"
}
```

**Withdraw Pi from the Bridge**

* **URL** : `/api/bridge/withdraw`
* **Method** : `POST`
* **Body**&#x20;

```json
{
  "wrappedToken": "wPi",
  "amount": 100,
  "sourceChain": "ethereum"
}
```

**Check Bridge Status**

* **URL** : `/api/bridge/status`
* **Method** : `GET`
* **Response**&#x20;

```json
{
  "status": "active",
  "supportedChains": ["ethereum", "binance", "polygon"]
}
```

### **FAQs** \<a name="faqs">\</a>

#### Q: What is the Bridge System?

A: The Bridge System enables cross-chain transfers of Pi tokens by locking Pi on one chain and minting wrapped tokens on another.

#### Q: Are wrapped Pi tokens secure?

A: Yes, wrapped Pi tokens are backed 1:1 by Pi and secured by smart contracts and decentralized oracles.

#### Q: Which blockchains are supported?

A: Currently, Ethereum, Binance Smart Chain, and Polygon are supported, with plans to expand to other chains.

#### Q: Can I trade wrapped Pi tokens on DEXs?

A: Yes, you can trade wrapped Pi tokens on decentralized exchanges like Uniswap or PancakeSwap.

#### Q: Where can I learn more about the Bridge System?

A: Visit the [Bridge System Documentation ](https://your-gitbook-space.gitbook.io/bridge-system).

***

For further inquiries or technical support, visit the[ Support Center .](../getting-started/quickstart/support.md)
