# **module 2: Setting Up Remix, MetaMask & Exploring Etherscan**

---

## **1. Installing & Using Remix**

### **What is Remix?**
Remix is an online IDE for developing, deploying, and testing Ethereum smart contracts written in Solidity.

### **Steps to Access Remix**
1. Open your browser and go to [Remix Ethereum](https://remix.ethereum.org/).
2. The IDE opens with a default workspace containing sample Solidity contracts.
3. Explore the **File Explorer**, **Solidity Compiler**, and **Deploy & Run Transactions** tabs.

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

