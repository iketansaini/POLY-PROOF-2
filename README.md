# My Circuit

A circuit to generate zero-knowledge circuits, proofs, and solidity verifiers

## Description

In this project we have designed a new zkSNARK circuit that implements some logical operations. We implemented the circuit and deployed a verifier on-chain to verify proofs generated from this circuit .

<img width="592" alt="image" src="https://github.com/s0HaNp/PolygonModule3/assets/95775561/e15a0cee-4fff-4571-8a63-8db8defcb4d8">

## Circuit Components

- AND Gate: The AND gate takes input signals A and B and produces an output signal, X, representing the logical AND of A and B.
- XOR Gate (Simulating NOT): The XOR gate takes input signals A and B and produces an output signal, Y, which simulates the logical NOT operation on A and B.
- OR Gate: The OR gate takes input signals X and Y and produces the final output signal, Q, representing the logical OR of X and Y.
  
## Deployment
### Installation
To install the necessary dependencies, run `npm i` in your project directory.

### Compilation
Compile the project by running `npx hardhat compile`. This will generate the `out` directory containing circuit intermediaries and the `MyCircuitVerifier.sol` contract.

### Proof Generation and Deployment

Use the command `npx hardhat run scripts/deploy.ts` to execute the deployment script. This script performs the following tasks:

1. Deploys the `MyCircuitVerifier.sol` contract on the blockchain.
2. Generates a proof using circuit intermediaries with the `generateProof()` function.
3. Creates calldata for the verification process using the `generateCallData()` function.
4. Calls the `verifyProof()` method on the deployed Verifier contract with the generated calldata to verify the proof.

By running this script, you will deploy the Verifier contract and verify the proof against the circuit, ensuring the correctness of your implementation.

### Conclusion 

In conclusion, this digital circuit implemented in circom version 2.0.0 demonstrates a basic combination of logical gates to perform fundamental logic operations. The circuit consists of three template components: AND, OR, and NOT, which are utilized in the main logic defined within the MyCircuit template.

By providing two input signals a and b, the circuit performs logical AND and NOT operations to generate two intermediate signals X and Y. These intermediate signals are then used to perform a logical OR operation, resulting in the final output signal Q.

This circuit can serve as a foundation for more complex digital systems and arithmetic logic units (ALUs). Its simplicity and modularity make it suitable for educational purposes, as well as for prototyping and testing various logic configurations.

To use the circuit, circom version 2.0.0 must be installed on the system, and the circuit needs to be compiled to generate the corresponding .json and .wasm files. With the circuit compiled, users can set input values for signals a and b, perform calculations, and retrieve the output value Q.

The project is provided under the permissive MIT License, granting users the freedom to use, modify, and distribute the circuit as they see fit.


