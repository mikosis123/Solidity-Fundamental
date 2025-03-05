# **Module 2: Setting Up Remix, MetaMask & Exploring Etherscan**

<details>
<summary><strong>1. Installing & Using Remix</strong></summary>

### **What is Remix?**
Remix is an online IDE for developing, deploying, and testing Ethereum smart contracts written in Solidity.

### **Steps to Access Remix**
1. Open your browser and go to [Remix Ethereum](https://remix.ethereum.org/).
2. The IDE opens with a default workspace containing sample Solidity contracts.
3. Explore the **File Explorer**, **Solidity Compiler**, and **Deploy & Run Transactions** tabs.

### **Creating Your First Smart Contract**
1. Click on the `+` icon in the file explorer.
2. Name the file `MyContract.sol`.
3. Copy and paste the following Solidity code:
   
   ```solidity
   // SPDX-License-Identifier: MIT
   pragma solidity ^0.8.20;

   contract HelloWorld {
       string public message = "Hello, Blockchain!";
   }
   ```
4. Click the **Solidity Compiler** tab and select **0.8.20**.
5. Click **Compile MyContract.sol**.
</details>

<details>
<summary><strong>2. Installing & Setting Up MetaMask</strong></summary>

### **What is MetaMask?**
MetaMask is a browser extension and mobile app that allows users to interact with the Ethereum blockchain.

### **Installing MetaMask**
1. Go to [MetaMask.io](https://metamask.io/).
2. Click **Download** and select your browser (Chrome, Firefox, Edge, or Brave).
3. Add the extension and click on the **MetaMask icon** in your browser.

### **Setting Up Your Wallet**
1. Click **Get Started** and select **Create a Wallet**.
2. Set a strong password.
3. **Secure Your Secret Recovery Phrase**:
   - Write down the 12-word phrase and store it safely.
   - Never share it with anyone!
4. Confirm the phrase and complete the setup.

### **Connecting MetaMask to Remix**
1. Open Remix and go to the **Deploy & Run Transactions** tab.
2. Under **Environment**, select **Injected Provider - MetaMask**.
3. MetaMask will prompt you to **connect your wallet**.
4. Approve the connection and choose an account.
</details>

<details>
<summary><strong>3. Exploring Etherscan</strong></summary>

### **What is Etherscan?**
Etherscan is a blockchain explorer that allows users to track Ethereum transactions, smart contracts, and wallet balances.

### **Exploring Transactions on Etherscan**
1. Open [Etherscan](https://etherscan.io/).
2. Copy and paste your **MetaMask wallet address** into the search bar.
3. View your **balance, transaction history, and smart contract interactions**.

### **Tracking a Transaction**
1. Send a small amount of ETH from MetaMask to another address.
2. Click on the **transaction hash** in MetaMask after sending.
3. This opens the **Etherscan transaction details**, showing:
   - **From & To addresses**
   - **Gas fee & Transaction cost**
   - **Block confirmation status**
</details>

<details>
<summary><strong>4. Summary & Next Steps</strong></summary>

✅ **Remix** helps you write and test smart contracts.
✅ **MetaMask** allows you to interact with the blockchain.
✅ **Etherscan** helps you track transactions and verify smart contracts.

### **Next Lesson: Deploying Smart Contracts on Testnets!** 🚀

</details>

[Back to Main Index](index.md)

