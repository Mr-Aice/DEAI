# DEAI Banking

**A Decentralized AI-Powered Crowdfunding and Micro-Banking Platform**

![Project Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-MIT-blue)
![Version](https://img.shields.io/badge/Version-1.0-orange)

## Overview

DEAI Banking is a decentralized crowdfunding and micro-banking platform designed to give students a transparent, trustworthy way to raise emergency and project funding directly from donors using cryptocurrency. Rather than sending funds straight to a campaign creator, the platform routes every donation into an **escrow smart contract**, releasing money only when the creator signs a withdrawal transaction validated against the available balance.

Before a campaign goes live, its funding request is automatically classified by an **AI model**, giving donors an immediate, trustworthy signal of what they are funding without relying solely on the creator's labeling.

---

## Core Features

*   **Wallet-Based Authentication:** Secure, password-less login using Web3 wallets (e.g., MetaMask).
*   **AI Campaign Classification:** Automatically categorizes campaigns (Medical Emergency, Disaster Relief, Tuition & Education, Research & Innovation, Community Project) with a confidence score.
*   **ThermalMesh AI Engine:** A custom thermally aware distributed inference engine. It monitors compute nodes processing the AI classification; if a node approaches its thermal ceiling, it checkpoints its state and reroutes remaining workloads to a cooler node, ensuring reliable performance without hardware overheating.
*   **Stablecoin Donations (USDT):** Donations are processed in USDT (an ERC-20 stablecoin) to keep funding values stable regardless of cryptocurrency market volatility.
*   **Smart Contract Escrow:** Funds are securely held in an Ethereum-compatible smart contract.
*   **Signature-Gated Withdrawals:** Campaign owners withdraw funds by signing transactions that validate the requested amount against their actual escrow balance.
*   **Decentralized Proof Storage:** Proof documents are uploaded to IPFS (via Fleek) ensuring permanent, decentralized access to campaign verification files.

---

## Technology Stack

### Frontend & Web3 Integration
*   **React:** Component-based UI framework for a responsive user experience.
*   **Thirdweb SDK:** Simplifies blockchain integration, wallet connection, and contract deployment.
*   **IPFS (Fleek):** Decentralized storage for campaign proof documents.

### Backend & Blockchain Layer
*   **Solidity:** Smart contract development for secure escrow and withdrawal logic.
*   **Ethereum Testnet:** Deployed on Holesky/Sepolia testnets for cost-effective execution.

### AI Classification Engine (ThermalMesh)
*   **Python:** Core language for the AI classification model and orchestration.
*   **PyTorch / scikit-learn:** Used for natural language processing and text classification.
*   **ThermalMesh Orchestrator:** Custom load-balancing middleware for distributed inference.

---

## Getting Started

### Prerequisites
*   [Node.js](https://nodejs.org/) installed
*   [Python 3.8+](https://www.python.org/) installed
*   A Web3 Wallet (e.g., [MetaMask](https://metamask.io/)) browser extension
*   Testnet ETH (Holesky/Sepolia) and Testnet USDT for testing

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/DEAI-Banking.git
    cd DEAI-Banking
    ```

2.  **Install Frontend Dependencies:**
    ```bash
    cd frontend
    npm install
    ```

3.  **Set up the AI Environment:**
    ```bash
    cd ../ai-engine
    pip install -r requirements.txt
    ```

4.  **Configure Environment Variables:**
    *   Create a `.env` file in the frontend directory with your Thirdweb Client ID and relevant network details.
    
5.  **Run the Application:**
    *   Start the ThermalMesh Orchestrator (Python): `python orchestrator.py`
    *   Start the React Frontend: `npm run dev`

---

## Project Team

*   **Muhammad Awais** - *Project Leader, Blockchain Developer, AI/ML Engineer, Frontend Developer, QA Engineer*
*   **Dr. Ghulam Mustafa** - *Internal Supervisor*
*   **Muhammad Younas** - *Project Coordinator*

*Submitted in partial fulfillment of the requirements for the degree of Bachelor in Computer Science at the University of the Punjab, Gujranwala Campus.*
