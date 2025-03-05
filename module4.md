# Module 4: Introduction to Solidity & Smart Contracts

<details>
<summary><strong> Declaring Variables and Functions in Solidity</strong></summary>

- 📝 **Introduction to Solidity syntax**
```
// SPDX-License-Identifier: MIT

pragma solidity //1. Enter solidity version here

//2. Create contract here

contract HelloWorld {

}
```
- 🔢 **How to declare variables** (`uint`, `string`, `address`, `bool`)
```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.19;

contract HelloWorld {
    // Declaring variables of different types
    uint public number = 42;         // Unsigned integer
    string public greeting = "Hello, World!";  // String
    address public owner;            // Ethereum address
    bool public isActive = true;     // Boolean
}
```

- 🏗 **State variables vs. local variables**

## Declaring Functions in Solidity

### **Function Visibility Types**

✅ **Public Functions (`public`)**
- Can be called **internally** (within the contract) and **externally** (from other contracts or users).
- Example: `publicFunction()` can be accessed by anyone.

✅ **Private Functions (`private`)**
- Can **only** be called inside the contract.
- Cannot be accessed by derived (inherited) contracts.
- Example: `_privateFunction()` is restricted to this contract only.

✅ **Internal Functions (`internal`)**
- Can **only** be called **inside the contract** and **by derived contracts** (inherited contracts).
- Similar to `private`, but allows child contracts to access the function.
- Example: `_internalFunction()` can be accessed within the contract and by inherited contracts.

✅ **External Functions (`external`)**
- Can **only** be called from outside the contract (not internally).
- Used when the function is meant for external calls.
- Example: `externalFunction()` can only be called externally.

### **Example Solidity Code**

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.19;

contract FunctionExample {
    uint private number = 10; // State variable

    // **Public Function** - Can be called by anyone
    function publicFunction() public view returns (uint) {
        return number;
    }

    // **Private Function** - Can only be called inside this contract
    function _privateFunction() private pure returns (string memory) {
        return "This is private";
    }

    // **Internal Function** - Can be called inside this contract and by inherited contracts
    function _internalFunction() internal pure returns (string memory) {
        return "This is internal";
    }

    // **External Function** - Can only be called from outside the contract
    function externalFunction() external pure returns (string memory) {
        return "This is external";
    }
}
```

### **Key Differences:**

| Function Type | Accessible Internally? | Accessible Externally? | Inherited by Child Contracts? |
| ------------- | ---------------------- | ---------------------- | ----------------------------- |
| `public`      | Yes                     | Yes                     | Yes                           |
| `private`     | Yes                     | No                      | No                            |
| `internal`    | Yes                     | No                      | Yes                           |
| `external`    | No                      | Yes                     | No                            |

### **How to Test:**

1. Call `publicFunction()` → Returns `number` (10).
2. Call `externalFunction()` **externally only**.
3. `_privateFunction()` **cannot** be called externally.
4. `_internalFunction()` **can be accessed by inherited contracts**.

This example keeps it simple while explaining function types in Solidity. 🚀


**💡 Interactive Task:**

- Use [Remix IDE](https://remix.ethereum.org/) to write and test a simple Solidity contract.

</details>
<details>
<summary><strong>State Mutability Keywords (Modifiers)</strong></summary>

- 🔍 **Understanding Function Mutability:**
  - `pure` → Cannot read or modify state variables.
  - `view` → Can read but not modify state variables.
  - `payable` → Allows the function to accept Ether.
- 🔥 **Example:**
  ```solidity
  contract MutabilityExample {
      uint public x;
      function setX(uint _x) public { x = _x; } // Modifies state
      function getX() public view returns (uint) { return x; } // Reads state
      function add(uint a, uint b) public pure returns (uint) { return a + b; } // No state access
  }
  ```
- 💡 **Interactive Task:**
  - Implement a function using all three mutability types and observe their effects.

</details>

<details>
<summary><strong>Variable Scope & How Visibility Specifiers Work in Solidity</strong></summary>

- 🔍 **Understanding where variables can be accessed** within a contract.
- 🏛 **Global, Local, and State Variables** in Solidity.
- 🧐 **Examples of scope limitations** and best practices.
- 🛠 **Debugging scope-related issues** in Solidity.

**💡 Interactive Task:**
- Modify a Solidity contract to include both global and local variables, then analyze their scope.

</details>

<details>
<summary><strong> How Visibility Specifiers Work</strong></summary>

- 👁 **Understanding Solidity visibility specifiers**: `public`, `private`, `internal`, and `external`.
- ⚠ **Security considerations** when defining visibility.

**💡 Interactive Task:**
- Analyze a real-world Solidity contract on [Remix IDE](https://remix.ethereum.org/)  and [Etherscan](https://etherscan.io/)  identify visibility specifiers used.

</details>





---

🔙 [Back to Main Index](index.md)
