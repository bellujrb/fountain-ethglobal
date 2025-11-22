# 🌊 Fountain - Automated Stablecoin Infrastructure on Arc

[![ETHGlobal](https://img.shields.io/badge/ETHGlobal-2024-blue)](https://ethglobal.com)
[![Arc Network](https://img.shields.io/badge/Built%20on-Arc-brightgreen)](https://circle.com/arc)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

> **Competing for:** 🏆 Best Smart Contracts on Arc with Advanced Stablecoin Logic ($4,000)

**Fountain** is building the infrastructure layer for automated tokenization in Brazil, now integrated with Circle's Arc blockchain. We provide an API-driven stablecoin factory that enables seamless real-world asset tokenization using USDC and EURC.

[🌐 Live Demo](https://app-fountain.vercel.app/) | [📖 Documentation](#) | [🎥 Video Demo](#)

---

## 🎯 The Problem

In 2024, over **1 billion reais** were tokenized in Brazil. But behind this growth lies chaos:

- ❌ Manual spreadsheet management
- ❌ Expensive intermediaries
- ❌ Slow, inefficient processes
- ❌ Artisanal deposit/withdrawal handling

Traditional tokenization requires multiple partners and manual intervention, making it costly and error-prone.

---

## 💡 Our Solution

Fountain automates the entire stablecoin issuance lifecycle through a simple API integrated with **Circle's Arc blockchain**:

\`\`\`javascript
// Automated stablecoin minting with USDC
await fountain.mint({
  amount: 1000,
  currency: 'USDC',
  recipient: walletAddress,
  collateral: 'auto' // Supports USDC, XRP, RLUSD, tokenized securities
});
\`\`\`

### Key Features

🔄 **Instant Minting:** Automated USDC/EURC issuance upon fiat deposit  
🔐 **Secure Escrow:** Multi-collateral support with smart contract guarantees  
🌐 **Cross-Chain Ready:** Integration with Circle's CCTP for interoperability  
📊 **Real-Time Transparency:** Auditable balance management for hundreds of clients  
⚡ **High Availability:** Built on Arc's robust Layer-1 infrastructure

---

## 🏗️ Architecture

### Smart Contract Logic on Arc

Our advanced stablecoin logic demonstrates:

1. **Conditional Minting:** Automated issuance based on collateral verification
2. **Cross-Chain Interoperability:** CCTP integration for multi-chain liquidity
3. **Collateral Management:** Dynamic collateral ratios with liquidation protection
4. **Batch Operations:** Gas-optimized bulk minting/burning

\`\`\`
┌─────────────────┐
│  Fiat Gateway   │
└────────┬────────┘
         │ PIX/Wire Transfer
         ▼
┌─────────────────┐      ┌──────────────────┐
│ Fountain API    │◄────►│  Arc Blockchain  │
│  (Backend)      │      │  Smart Contracts │
└────────┬────────┘      └──────────────────┘
         │                        │
         │                        │ USDC/EURC
         ▼                        ▼
┌─────────────────┐      ┌──────────────────┐
│   Custodial     │      │  Circle Gateway  │
│    Wallets      │◄────►│      & CCTP      │
└─────────────────┘      └──────────────────┘
\`\`\`

### Integration with Circle's Ecosystem

- **USDC as Gas Token:** Native integration with Arc's USDC-powered operations
- **CCTP Integration:** Cross-chain USDC transfers for global liquidity
- **Circle Gateway:** Fiat on/off-ramp connectivity
- **EVM Compatibility:** Standard Solidity smart contracts for maximum composability

---

## 🚀 What We've Built

### Already Delivered

✅ **Smart Contracts on Arc** - Advanced stablecoin logic with conditional automation  
✅ **Python & JavaScript SDKs** - Easy integration for developers  
✅ **Landing Page** - [app-fountain.vercel.app](https://app-fountain.vercel.app/)  
✅ **Full Documentation** - Comprehensive API and SDK guides  
✅ **Backend Integration** - Arc blockchain + database infrastructure  
✅ **Custodial Wallet Management** - Secure key management system  
✅ **Multi-Collateral Escrow** - USDC, XRP, RLUSD, and tokenized securities support

### Roadmap

🔄 Additional exchange providers integration  
🔄 Multiple payment gateway support  
🔄 Enhanced collateral types (tokenized Brazilian public securities)  
🔄 Advanced CCTP routing strategies

---

## 💼 Business Model

Our pilot partner **Sônica** manages two clients moving **~$750,000 USD monthly**:

- **Transaction Fee:** 0.1% - 0.5% per issuance
- **Subscription Plans:** Premium dashboards and priority support
- **Target:** 5 tokenization partners, $20K MRR in 12 months

**Global tokenization market:** Projected to reach **$16 trillion USD**

---

## 🛠️ Technical Stack

- **Blockchain:** Arc Layer-1 (Circle)
- **Smart Contracts:** Solidity (EVM-compatible)
- **Stablecoins:** USDC, EURC
- **Backend:** Node.js + TypeScript
- **Database:** PostgreSQL
- **SDKs:** Python, JavaScript/TypeScript
- **Infrastructure:** Vercel, AWS

---

## 👥 Team

Our team has **5+ years of blockchain infrastructure experience** and has delivered **2 projects for DREX** (Brazil's Central Bank Digital Currency pilot).

---

## 📊 ETHGlobal Submission

### Qualification Requirements

✅ **Functional MVP:** Live demo at [app-fountain.vercel.app](https://app-fountain.vercel.app/)  
✅ **Architecture Diagram:** See above  
✅ **Video Demonstration:** [Watch here](#)  
✅ **GitHub Repository:** You're here!  
✅ **Detailed Documentation:** Available in \`/docs\`

### How We Use Circle's Tools

1. **Arc Blockchain:** All smart contracts deployed on Arc L1
2. **USDC/EURC:** Primary stablecoins for Brazilian tokenization
3. **CCTP:** Cross-chain transfers for international liquidity
4. **Circle Gateway:** Fiat on-ramp integration (in progress)

---

## 🚦 Getting Started

\`\`\`bash
# Install dependencies
npm install

# Configure Arc network
cp .env.example .env
# Add your Arc RPC endpoint and private key

# Deploy contracts
npm run deploy:arc

# Run tests
npm test

# Start the API
npm run dev
\`\`\`

### Quick Integration

\`\`\`javascript
import { Fountain } from '@fountain/sdk';

const fountain = new Fountain({
  network: 'arc-mainnet',
  apiKey: process.env.FOUNTAIN_API_KEY
});

// Mint USDC-backed stablecoin
const tx = await fountain.mint({
  amount: 1000,
  asset: 'USDC',
  recipient: '0x...'
});
\`\`\`

---

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details

---

## 🔗 Links

- [Live Application](https://app-fountain.vercel.app/)
- [Documentation](#)
- [Video Demo](#)
- [ETHGlobal Project Page](#)
- [Circle Arc Documentation](https://docs.circle.com/arc)

---
