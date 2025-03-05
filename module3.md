# **Module 3: Ethereum and Smart Contracts**

---

<details>
<summary> Introduction to Ethereum</summary>

### 🌟 What is Ethereum?

- **Ethereum** is a decentralized blockchain platform for executing **smart contracts** and **decentralized applications (DApps)**.
- The **Ethereum Virtual Machine (EVM)** is the runtime environment responsible for executing smart contracts across the Ethereum network.

</details>

<details>
<summary> Gas Fees and Transactions</summary>

### 🔥 What is Gas?

- Gas is a unit that measures the computational effort required to process transactions or execute smart contracts.

### 🤔 Why is Gas Needed?

- It prevents spam and ensures fair resource allocation in the network.

### 💰 How Gas Fees Are Calculated:

- Formula: `Total Fee = Gas Limit × Gas Price`
- Gas price is measured in **gwei** (1 gwei = 0.000000001 ETH).
- **Base Fee + Priority Fee (Tip) = Total Fee** (Post EIP-1559 upgrade).

### 🧾 Who Pays Gas Fees?

- The sender of the transaction covers the cost.

</details>

<details>
<summary> What are Smart Contracts?</summary>

### 🔹 Definition:

- **Smart contracts** are self-executing programs with predefined rules, eliminating the need for intermediaries.

### 📌 Use Cases:

- **💸 DeFi (Decentralized Finance)** – Automated lending, borrowing, and trading.
- **🎨 NFTs (Non-Fungible Tokens)** – Digital ownership of assets like art and music.
- **🏛 DAOs (Decentralized Autonomous Organizations)** – Community-governed organizations using smart contracts.

</details>

<details>
<summary> Solidity Programming Language</summary>

### 🏗 Solidity Overview:

- **Solidity** is the main programming language for writing Ethereum smart contracts.
- **Solidity Documentation**: [Official Solidity Documentation](https://soliditylang.org/docs/)
### ⚙️ Key Features of Solidity:

- Statically typed, contract-oriented.
- Supports inheritance, modifiers, and libraries.

### 🔠 Basic Solidity Syntax:

- **Data types:** (`uint`, `address`, `string`, `bool`)
- **Functions:** (`public`, `private`, `view`, `pure`)
- **Control structures:** (`if-else`, `for`, `while`, `require`, `assert`)

</details>

<details>
<summary>📝 Writing Your First Smart Contract</summary>

### 🏁 Hello World Smart Contract:

- Writing a simple contract that stores and retrieves a message.
- Understanding `msg.sender`, `public`, and `state variables`.

### 🚀 Deploying a Smart Contract:

- **Remix IDE** (a web-based Solidity editor).
- **Foundry** (a modern toolchain for Ethereum development).

</details>

---

📌 **Next Steps:** Start deploying your smart contracts on a testnet! 🚀  
🔙 [Back to Main Index](index.md)
