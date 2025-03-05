
# Module 8: Smart Contract Interaction & Transactions

## **How to Call Contracts and Use the Fallback Function**

In Solidity, you can call functions from other contracts, enabling interaction between contracts on the Ethereum blockchain. A fallback function allows a contract to accept Ether and react when it receives transactions without matching function calls.

### **Example: Calling Another Contract**

```solidity
pragma solidity ^0.8.19;

contract Receiver {
    uint public balanceReceived;

    // Function to receive Ether
    receive() external payable {
        balanceReceived += msg.value;
    }
}

contract Sender {
    address payable receiverAddress;

    constructor(address payable _receiverAddress) {
        receiverAddress = _receiverAddress;
    }

    function sendEther() public payable {
        receiverAddress.transfer(msg.value); // Send Ether to the Receiver contract
    }
}
```

### **Fallback Function Example**

A fallback function is executed when a contract is sent Ether without any data or when a non-existent function is called.

```solidity
pragma solidity ^0.8.19;

contract FallbackExample {
    // Fallback function to accept Ether
    fallback() external payable {
        // Logic here
    }
}
```

---

## **How to Send and Receive Ether**

Sending and receiving Ether is an essential operation in Solidity. Contracts can receive Ether via the `receive` or `fallback` functions and send Ether using the `transfer` or `send` methods.

### **Receiving Ether Example**

```solidity
pragma solidity ^0.8.19;

contract EtherReceiver {
    uint public balanceReceived;

    // Function to receive Ether
    receive() external payable {
        balanceReceived += msg.value;
    }
}
```

### **Sending Ether Example**

```solidity
pragma solidity ^0.8.19;

contract EtherSender {
    address payable public recipient;

    constructor(address payable _recipient) {
        recipient = _recipient;
    }

    function sendEther() public payable {
        recipient.transfer(msg.value); // Send Ether to the recipient
    }
}
```

---

## **Solidity Libraries**

Solidity libraries are reusable pieces of code that can be deployed and used by multiple contracts. They allow for efficient and gas-saving interactions by sharing common functionality.

### **Example: Using a Library**

```solidity
pragma solidity ^0.8.19;

library MathLibrary {
    function add(uint a, uint b) public pure returns (uint) {
        return a + b;
    }
}

contract Calculator {
    using MathLibrary for uint;

    function calculateSum(uint a, uint b) public pure returns (uint) {
        return a.add(b); // Using MathLibrary function
    }
}
```

---

## **Events and Logs in Solidity**

Events are an essential way to log data on the blockchain. They allow external consumers (like DApps) to listen to specific events and react accordingly.

### **Example: Emitting an Event**

```solidity
pragma solidity ^0.8.19;

contract EventExample {
    event Transfer(address indexed from, address indexed to, uint256 value);

    function transfer(address to, uint256 value) public {
        emit Transfer(msg.sender, to, value); // Emitting an event
    }
}
```

### **Listening to Events**

Events are logged on the blockchain and can be tracked using tools like Web3.js or Ethers.js, which listen to contract events in real-time.

---

## **Time Logic in Solidity**

Solidity provides built-in functions to handle time and block-related data, such as block timestamps, block numbers, and gas usage.

### **Example: Using Block Timestamp**

```solidity
pragma solidity ^0.8.19;

contract TimeLogic {
    uint public startTime;

    constructor() {
        startTime = block.timestamp; // Store contract creation timestamp
    }

    function getElapsedTime() public view returns (uint) {
        return block.timestamp - startTime; // Calculate elapsed time since contract creation
    }
}
```

### **Example: Delayed Actions**

```solidity
pragma solidity ^0.8.19;

contract TimedTransfer {
    address public recipient;
    uint public releaseTime;

    constructor(address _recipient, uint _delay) {
        recipient = _recipient;
        releaseTime = block.timestamp + _delay; // Delay transfer by _delay seconds
    }

    function releaseFunds() public {
        require(block.timestamp >= releaseTime, "Not yet time to release funds");
        payable(recipient).transfer(address(this).balance);
    }
}
```

---

## **Interactive Tasks:**

- **Task 1:** Create a contract that interacts with another contract by sending and receiving Ether using the `receive` and `fallback` functions.
- **Task 2:** Write a contract that uses a library to perform arithmetic calculations and deploy it on Remix IDE.
- **Task 3:** Implement a contract that emits events upon transfers and test it using Web3.js or Ethers.js to listen to these events.
- **Task 4:** Build a contract that uses block timestamp to delay actions (e.g., releasing funds after a certain period).

---

[Back to Main Index](index.md)
