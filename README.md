
# RAMC: Resource Allocation via Multi-Party Computation

RAMC is a privacy-preserving resource matching system that uses Secure Multi-Party Computation (MPC), ATLAS, and WebAssembly to identify complementary partnerships without revealing participants' private capabilities.

The project demonstrates how independent countries can collaborate and make strategic decisions while keeping their resource information confidential.

## Overview

RAMC simulates an international cooperation scenario where each country privately provides a vector representing four strategic capabilities:

- **Defense**
- **Logistics**
- **Intelligence**
- **Diplomacy**

The system evaluates resource deficits and surpluses to identify partnerships that provide the greatest mutual benefit.

## How It Works

1. **Join a session:** Participants connect to a shared session and represent different countries.
2. **Enter private capabilities:** Each participant provides their resource values.
3. **Secure computation:** The system uses MPC to evaluate potential partnerships without revealing the original resource vectors.
4. **Receive results:** Each participant receives their recommended partner.

## Technologies

| Technology | Purpose |
|---|---|
| MP-SPDZ | Framework for secure multi-party computation |
| Shamir Secret Sharing | Protects private inputs by distributing secret shares |
| ATLAS | MPC protocol for secure distributed computation |
| WebAssembly | Enables the MPC runtime to execute in the browser |
| Emscripten | Compiles the native C++ runtime for WebAssembly |
| WebRTC | Enables peer-to-peer communication between participants |
| WebSocket | Coordinates participants and session connections |

## Privacy and Security

RAMC is designed to protect participants' confidential information throughout the matching process.

- Private resource values are processed using secret sharing and MPC.
- Participants communicate through encrypted channels.
- The signaling server coordinates connections without receiving the complete private resource vectors.
- The intended output reveals only each participant's recommended partner.

The system operates under the security assumptions of its selected MPC protocol.

## Research and Evaluation

RAMC investigates the practical performance of MPC by examining how execution time, communication rounds, and data transfer change as the number of participants and resource dimensions increases.

The project evaluates the trade-offs between security, accessibility, and computational efficiency.

## Project Background

RAMC builds on the following open-source research projects:

- **[MP-SPDZ](https://github.com/data61/MP-SPDZ)** – A framework for secure multi-party computation.
- **[webSPDZ](https://eprint.iacr.org/2025/487)** – A browser-based implementation of MP-SPDZ.

RAMC contributes a private resource-matching application, an interactive browser interface, and experimental performance evaluation.

## Project Status

**Research Prototype**

Source code, setup instructions, and supporting documentation will be added as the repository is prepared for publication.
