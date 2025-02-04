Escrow Smart Contract & Frontend Project

Overview

This project is a decentralized escrow system that ensures secure transactions between parties by leveraging blockchain technology. The system consists of a smart contract that handles the escrow logic and a frontend application for users to interact with it.

Project Structure

/escrowproject
  /backend    # Smart contract implementation (Rust)
  /frontend   # User interface (Next.js, React, TypeScript)

Features

Secure escrow-based transactions between buyers and sellers

Blockchain-based trustless transactions

Integration with MultiversX SDK for Web3 functionality

User authentication and wallet connection

Smart contract interaction via frontend

Technologies Used

Backend (Smart Contract)

Language: Rust

Blockchain: MultiversX (formerly Elrond)

Smart Contract Framework: MultiversX Rust SDK

Frontend

Framework: Next.js

UI Library: React, TailwindCSS

Web3 SDK: MultiversX SDK

State Management: React Hooks

Installation & Setup

Prerequisites

Node.js (>= 16.x)

Rust & Cargo (for smart contract development)

MultiversX CLI

Metamask or xPortal Wallet

1. Clone the repository

git clone https://github.com/EnesGoktekin/escrowproject.git
cd escrowproject

2. Set Up Backend (Smart Contract)

cd backend
cargo build
cargo test  # Run tests

3. Deploy Smart Contract

mxpy contract deploy --project backend --recall-nonce --gas-limit=5000000 --pem=wallet.pem --proxy=https://devnet-gateway.multiversx.com

Replace wallet.pem with your actual wallet private key.

4. Set Up Frontend

cd ../frontend
npm install
npm run dev  # Start local development server

Then, open http://localhost:3000 in your browser.

Environment Variables

Create a .env file inside the frontend folder with the following:

NEXT_PUBLIC_CONTRACT_ADDRESS=0xYourSmartContractAddress
NEXT_PUBLIC_RPC_URL=https://your-blockchain-rpc

Usage

Connect your wallet using xPortal or Metamask.

Initiate a transaction by placing funds in escrow.

The smart contract holds the funds until conditions are met.

Upon agreement, funds are released securely.

Contribution

Feel free to fork the repo and submit pull requests! 🚀