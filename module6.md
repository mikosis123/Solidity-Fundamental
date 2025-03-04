## **Module 6: Solidity Data Types & Functions**

# **Solidity: Typing, Data Structures, and Error Handling**

---

<details>
<summary><strong>How Typing Works</strong></summary>

- 🎯 **Static Typing in Solidity**
  - Solidity is a statically typed language, meaning variable types must be declared explicitly.
  - Example:
    ```solidity
    uint256 number = 10;
    bool isActive = true;
    ```

- 🔥 **Type Safety:**
  - Prevents unintended operations and increases contract security.
  - Data type conversions must be done explicitly.

- 💡 **Interactive Task:**
  - Declare and assign different types of variables in Solidity.

</details>

<details>
<summary><strong>Solidity Data Types</strong></summary>

- 🏗 **Value Types:**
  - `uint`, `int`, `bool`, `address`, `bytes`, `enum`.
  - Example:
    ```solidity
    uint256 age = 25;
    bool isAvailable = false;
    ```

- 🗂 **Reference Types:**
  - `string`, `array`, `mapping`, `struct`.
  - Example:
    ```solidity
    struct Person {
        string name;
        uint age;
    }
    ```

- 💡 **Interactive Task:**
  - Create a contract that declares and manipulates different data types.

</details>

<details>
<summary><strong>How to Declare and Initialize Arrays in Solidity</strong></summary>

- 🔢 **Array Types:**
  - **Fixed-size arrays**: Defined with a set length.
  - **Dynamic arrays**: Can grow in size.

- 🔥 **Examples:**
  ```solidity
  uint256[5] fixedArray;  // Fixed-size
  uint256[] dynamicArray; // Dynamic
  ```

- 🏗 **Adding and Removing Elements:**
  ```solidity
  dynamicArray.push(10); // Add element
  dynamicArray.pop();    // Remove last element
  ```

- 💡 **Interactive Task:**
  - Implement a contract with dynamic and fixed arrays, adding and removing elements.

</details>

<details>
<summary><strong>What are Function Modifiers?</strong></summary>

- 🔍 **Definition:**
  - Modifiers are used to alter function behavior.
  - Reduce code duplication and improve readability.

- 🔥 **Example:**
  ```solidity
  modifier onlyOwner() {
      require(msg.sender == owner, "Not the contract owner");
      _;
  }
  ```

- 💡 **Interactive Task:**
  - Create a contract with a function modifier that restricts access to a specific user.

</details>

<details>
<summary><strong>Error Handling in Solidity - require, assert, revert</strong></summary>

- 🚨 **Error Handling Functions:**
  - `require(condition, "error message")` → Checks conditions and reverts if false.
  - `assert(condition)` → Used for internal errors and invariants.
  - `revert("error message")` → Custom error handling.

- 🔥 **Example:**
  ```solidity
  function withdraw(uint amount) public {
      require(amount <= balance, "Insufficient funds");
      balance -= amount;
  }
  ```

- 💡 **Interactive Task:**
  - Implement a Solidity function using `require`, `assert`, and `revert` for error handling.

</details>

</details>

---

[Back to Main Index](index.md)
