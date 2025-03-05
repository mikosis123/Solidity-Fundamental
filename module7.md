# **module 7 :Advanced Solidity Concepts: Inheritance, Typing & Encoding**

---

<details>
<summary><strong>Inheritance in Solidity</strong></summary>

- 🏗 **Definition:** Solidity supports contract inheritance, allowing contracts to extend functionalities of other contracts.
- 🔄 **Single & Multi-level Inheritance:**

  - **Single Inheritance:** A contract inherits from one base contract.
  - **Multi-level Inheritance:** A contract inherits from another that has already inherited a base contract.

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
  - Implement a multi-level inheritance structure with function overrides.

</details>

<details>
<summary><strong>Inheritance with Constructor Parameters</strong></summary>

- 🎯 **Passing Parameters to Parent Constructors:**

  - Constructors from parent contracts can be called in the child contract.
  - Solidity supports parameterized inheritance for initializing state variables.

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
  - Create a parent contract that takes an address parameter and passes it to a child contract.

</details>

<details>
<summary><strong>Type Conversion and Type Casting in Solidity</strong></summary>

- 🔄 **Implicit & Explicit Conversion:**

  - **Implicit:** Automatically converts smaller types to larger types (e.g., `uint8` to `uint256`).
  - **Explicit:** Requires manual conversion between types.

- 🔥 **Example:**

  ```solidity
  uint8 smallNumber = 10;
  uint256 largeNumber = smallNumber; // Implicit conversion
  uint8 convertedBack = uint8(largeNumber); // Explicit conversion
  ```

- 💡 **Interactive Task:**
  - Try casting between different integer types and analyze gas costs.

</details>

<details>
<summary><strong>How to Work with Floating Point Numbers in Solidity</strong></summary>

- ⚠ **Solidity does NOT support floating-point arithmetic.**
- 📌 **Alternative:** Use fixed-point math by multiplying values by a scaling factor.

- 🔥 **Example:**

  ```solidity
  contract FixedPointMath {
      uint256 public scale = 10**18;
      function divide(uint256 a, uint256 b) public view returns (uint256) {
          return (a * scale) / b; // Emulating floating point division
      }
  }
  ```

- 💡 **Interactive Task:**
  - Implement a function that performs fixed-point multiplication and division.

</details>

<details>
<summary><strong>Hashing, ABI Encoding and Decoding</strong></summary>

- 🔒 **Hashing Functions:** Solidity supports cryptographic hashing (e.g., `keccak256`).
- 🔄 **ABI Encoding:** Converts Solidity data into bytes format for contract interaction.
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
  - Create a contract that hashes two values and verifies their integrity.

</details>

---

🔙 [Back to Main Index](index.md)
