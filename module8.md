## **Module 8: Smart Contract Interaction & Transactions**

---

<details>
<summary><strong>Inheritance in Solidity</strong></summary>

- 🏗 **Definition:** Solidity allows contract inheritance, enabling code reuse and modularity.
- 🔄 **Types of Inheritance:**
  - **Single Inheritance:** A contract inherits from one base contract.
  - **Multiple Inheritance:** A contract inherits from multiple base contracts.
  - **Hierarchical Inheritance:** Multiple contracts inherit from a single base contract.
- 🔥 **Example:**
  ```solidity
  contract Parent {
      uint public value;
      function setValue(uint _value) public {
          value = _value;
      }
  }
  
  contract Child is Parent {
      function getValue() public view returns (uint) {
          return value;
      }
  }
  ```
- 💡 **Interactive Task:**
  - Implement multiple inheritance and resolve method conflicts.

</details>

<details>
<summary><strong>Inheritance with Constructor Parameters</strong></summary>

- 🎯 **Passing Parameters to Parent Constructors:**
  - Solidity allows passing parameters from child to parent constructors.
  - The `is` keyword is used to inherit contracts and initialize parent constructor.
- 🔥 **Example:**
  ```solidity
  contract Parent {
      uint public value;
      constructor(uint _value) {
          value = _value;
      }
  }
  
  contract Child is Parent(100) {
      function getValue() public view returns (uint) {
          return value;
      }
  }
  ```
- 💡 **Interactive Task:**
  - Implement an inheritance model where multiple child contracts pass different constructor parameters to a single parent contract.

</details>

<details>
<summary><strong>Type Conversion and Type Casting in Solidity</strong></summary>

- 🔄 **Implicit & Explicit Conversion:**
  - **Implicit:** Safe conversions from smaller to larger data types (e.g., `uint8` to `uint256`).
  - **Explicit:** Requires manual conversion (e.g., `uint256` to `uint8`).
- 🔥 **Example:**
  ```solidity
  uint8 smallNum = 42;
  uint256 largeNum = smallNum; // Implicit conversion
  uint8 convertedBack = uint8(largeNum); // Explicit conversion
  ```
- 💡 **Interactive Task:**
  - Convert between integer types and analyze gas costs.

</details>

<details>
<summary><strong>How to Work with Floating Point Numbers in Solidity</strong></summary>

- ⚠ **No Native Floating-Point Support:** Solidity does not support floating-point arithmetic.
- 📌 **Solution:** Use fixed-point arithmetic by multiplying values by a scaling factor.
- 🔥 **Example:**
  ```solidity
  contract FixedPointMath {
      uint256 public scale = 10**18;
      function divide(uint256 a, uint256 b) public view returns (uint256) {
          return (a * scale) / b;
      }
  }
  ```
- 💡 **Interactive Task:**
  - Implement multiplication and division using fixed-point math.

</details>

<details>
<summary><strong>Hashing, ABI Encoding and Decoding</strong></summary>

- 🔒 **Hashing Functions:** Solidity supports `keccak256`, `sha256`, and `ripemd160` for hashing data.
- 🔄 **ABI Encoding:** Converts Solidity data into bytes format for contract interactions.
- 🔁 **ABI Decoding:** Converts bytes back into Solidity data types.
- 🔥 **Example:**
  ```solidity
  contract HashingExample {
      function hashData(string memory data) public pure returns (bytes32) {
          return keccak256(abi.encodePacked(data));
      }
  }
  ```
- 💡 **Interactive Task:**
  - Implement a contract that hashes and verifies data integrity.

</details>

---

[Back to Main Index](index.md)
