# ** module 5: Contract Structure & State Management**

---



<details>
<summary><strong>What are Constructors?</strong></summary>

- 🏗 **Definition:** A constructor is a special function in Solidity that is executed only once when the contract is deployed.
- 🎯 **Purpose:** Used to initialize contract state variables.
- 📝 **Key Features:**
  - Defined using `constructor` keyword.
  - Cannot be called again after deployment.
  - Often used for setting immutable values.
- 🔥 **Example:**
  ```solidity
  contract Example {
      uint public value;
      constructor(uint _value) {
          value = _value;
      }
  }
  ```
- 💡 **Interactive Task:**
  - Write a contract with a constructor that sets an initial owner address.

</details>

<details>
<summary><strong>Interfaces and Abstract Contracts</strong></summary>

- 🖧 **Interfaces:**
  - Define a contract structure without implementing functions.
  - Used for interoperability between different contracts.
  - Cannot have state variables or constructors.
  - Example:
    ```solidity
    interface Token {
        function transfer(address recipient, uint amount) external;
    }
    ```

- 🏗 **Abstract Contracts:**
  - Allow function definitions without implementation.
  - Cannot be deployed on their own; used as base contracts.
  - Support inheritance for extending functionalities.
  - Example:
    ```solidity
    abstract contract Base {
        function doSomething() public virtual;
    }
    ```
- 💡 **Interactive Task:**
  - Create an interface for a voting system and implement it in a contract.

</details>

<details>
<summary><strong>What is Contract State?</strong></summary>

- 🔄 **Definition:** A contract’s state refers to its stored variables and values at a given time.
- 🗂 **State Variables:** Stored permanently on the blockchain and can change over time.
- 🚀 **Examples of State in Action:**
  - Token balances in an ERC-20 contract.
  - Ownership status in an NFT contract.
  - Voting tallies in a DAO.
- 🔥 **Example:**
  ```solidity
  contract StateExample {
      uint public counter;
      function increment() public {
          counter += 1;
      }
  }
  ```
- 💡 **Interactive Task:**
  - Modify a contract’s state and observe changes on Remix.

</details>



<details>
<summary><strong>Data Locations – Storage, Memory, and Stack</strong></summary>

- 📌 **Storage:**
  - Data stored permanently on the blockchain.
  - Used for state variables.
  - Higher gas cost.

- 🔧 **Memory:**
  - Temporary data storage used within functions.
  - Automatically deleted after function execution.
  - Used for dynamic data structures like arrays and structs.

- 🏗 **Stack:**
  - Small temporary storage for variables.
  - Limited space, efficient for small calculations.

- 🔥 **Example:**
  ```solidity
  contract DataLocations {
      string public storedData = "Blockchain"; // Stored permanently
      
      function getMemoryData() public pure returns (string memory) {
          return "Temporary Data"; // Stored temporarily in memory
      }
  }
  ```
- 💡 **Interactive Task:**
  - Write a function that takes an array as an argument and modifies it in `memory`.

</details>

</details>

---

[Back to Main Index](index.md)
