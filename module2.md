# Module 2: Ethereum and Smart Contracts

---



### Introduction to Ethereum

- **Ethereum** is a decentralized blockchain platform for executing **smart contracts** and **decentralized applications (DApps)**.
- The **Ethereum Virtual Machine (EVM)** is the runtime environment responsible for executing smart contracts across the Ethereum network.

### Gas Fees and Transactions

- **What is Gas?**
  - Gas is a unit that measures the computational effort required to process transactions or execute smart contracts.
- **Why is Gas Needed?**
  - It prevents spam and ensures fair resource allocation in the network.
- **How Gas Fees Are Calculated:**
  - Formula: `Total Fee = Gas Limit × Gas Price`
  - Gas price is measured in **gwei** (1 gwei = 0.000000001 ETH).
  - **Base Fee + Priority Fee (Tip) = Total Fee** (Post EIP-1559 upgrade).
- **Who Pays Gas Fees?**
  - The sender of the transaction covers the cost.

### What are Smart Contracts?

- **Smart contracts** are self-executing programs with predefined rules, eliminating the need for intermediaries.
- **Use Cases:**
  - **DeFi (Decentralized Finance)** – Automated lending, borrowing, and trading.
  - **NFTs (Non-Fungible Tokens)** – Digital ownership of assets like art and music.
  - **DAOs (Decentralized Autonomous Organizations)** – Community-governed organizations using smart contracts.

### Solidity Programming Language

- **Solidity** is the main programming language for writing Ethereum smart contracts.
- **Key Features of Solidity:**
  - Statically typed, contract-oriented.
  - Supports inheritance, modifiers, and libraries.
- **Basic Solidity Syntax Includes:**
  - Data types (`uint`, `address`, `string`, `bool`).
  - Functions (`public`, `private`, `view`, `pure`).
  - Control structures (`if-else`, `for`, `while`, `require`, `assert`).

### Writing Your First Smart Contract

- **Hello World Smart Contract:**
  - Writing a simple contract that stores and retrieves a message.
  - Understanding `msg.sender`, `public`, and `state variables`.
- **Deploying a Smart Contract:**
  - Using **Remix IDE** (a web-based Solidity editor).
  - Using **Foundry** (a modern toolchain for Ethereum development).

### Example: Teacher Incorporating an External Website

Imagine a teacher demonstrating how to fetch Ethereum gas prices dynamically from an external website like [Etherscan](https://etherscan.io/gastracker):

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract GasPriceChecker {
    string public infoSource = "Etherscan Gas Tracker";
    string public url = "https://etherscan.io/gastracker";

    function getGasPriceInfo() public view returns (string memory, string memory) {
        return (infoSource, url);
    }
}
```

This simple contract stores a reference to Etherscan's gas tracker. In a classroom setting, the teacher could explain how external sources help developers make informed decisions about gas fees when deploying or executing contracts.

---

[Back to Main Index](index.md)
