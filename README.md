## Zero-Knowledge Circuit and Proof Generation System
This repository contains a sophisticated zero-knowledge circuit generation system capable of creating proofs and Solidity verifiers.


## #Overview
Within this project, we've developed an innovative zkSNARK (Zero-Knowledge Succinct Non-Interactive Argument of Knowledge) circuit. This circuit is designed to execute various logical operations. We've not only conceptualized and implemented this circuit but have also deployed a verifier on-chain to facilitate the validation of proofs derived from this circuit.
<img width="592" alt="image" src="https://github.com/s0HaNp/PolygonModule3/assets/95775561/e15a0cee-4fff-4571-8a63-8db8defcb4d8">


Circuit

### Circuit Components
The key components of our zkSNARK circuit include:

'AND Gate': This gate processes input signals A and B, producing an output signal X that represents the logical AND of A and B.
'XOR Gate (Simulating NOT)': Taking inputs A and B, this XOR gate produces an output signal Y, simulating the logical NOT operation on A and B.
'OR Gate': Inputting signals X and Y, this gate generates the final output signal Q, symbolizing the logical OR of X and Y.
## Deployment Instructions
## Prerequisites
Prior to deployment, ensure that you have the required dependencies. To do this, run the command npm i within your project directory.

### Compilation Process
Compile the project by executing npx hardhat compile. This action will generate the out directory housing circuit intermediaries, along with the MyCircuitVerifier.sol contract.

### Proof Generation and Deployment
To accomplish proof generation and deployment, execute the command npx hardhat run scripts/deploy.ts. This script performs several essential tasks:

Deploys the MyCircuitVerifier.sol contract onto the blockchain.
Generates a proof using circuit intermediaries via the generateProof() function.
Creates the required calldata for the verification process through the generateCallData() function.
Initiates a call to the verifyProof() method on the deployed Verifier contract, utilizing the generated calldata to authenticate the proof.
Through this script, you will successfully deploy the Verifier contract and verify the proof against the underlying circuit, validating the correctness of your implementation.


