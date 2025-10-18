  # 💧 Flow EVM Faucet Smart Contract

A simple, secure **Faucet Smart Contract** designed for the **Flow EVM Testnet** (or any EVM-compatible blockchain).  
It allows developers and testers to **request native tokens or ERC20 test tokens** with cooldown control, owner administration, and transparent event logs.

---

## 🚀 Overview

This faucet supports:

- ✅ Native token distribution (e.g., FLOW testnet coins)
- ✅ ERC20 test token distribution
- ✅ Per-user cooldown enforcement
- ✅ Owner-only controls (pause, withdraw, settings)
- ✅ Full transparency through on-chain events

The contract is ideal for **developers**, **hackathons**, and **test environments** where controlled test token distribution is needed.

---

## ⚙️ Features

| Feature | Description |
|----------|-------------|
| 💰 **Native Token Faucet** | Dispenses native testnet tokens (e.g., FLOW-evm test coins). |
| 🪙 **ERC20 Token Support** | Works with any ERC20-compliant test token. |
| 🕒 **Cooldown Mechanism** | Prevents spam requests (customizable per user). |
| 🔒 **Admin Controls** | Owner can pause, update settings, withdraw, and change ownership. |
| 📜 **Events & Logs** | All requests and owner actions are emitted on-chain. |

---

## 🧩 Smart Contract Details

### **Contract Name**
`SimpleFaucet`

### **Compiler Version**
Solidity `^0.8.19`

### **License**
MIT

---

## 🏗️ Deployment Instructions

### 1. **Using Remix IDE**

1. Open [Remix](https://remix.ethereum.org/)
2. Create a new file named `SimpleFaucet.sol`
3. Paste the contract code into it.
4. Select **Solidity Compiler** → version `0.8.19` and click **Compile**.
5. Go to **Deploy & Run Transactions** tab.
6. Choose **Injected Provider - MetaMask**.
7. Connect to **Flow EVM Testnet**.
8. Deploy with parameters:
   - `_cooldownSec`: e.g., `3600` (1 hour)
   - `_nativeAmount`: e.g., `10000000000000000` (0.01 native token)

---

## 💡 Example Usage

### **1. Fund the Faucet**

Send some testnet FLOW (EVM) tokens or ERC20 tokens to the contract address.

### **2. Request Tokens**

#### For Native Tokens:
```solidity
requestNative()
