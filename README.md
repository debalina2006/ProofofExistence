# 📜 Proof of Existence on Stellar (Soroban)

## 🚀 Project Description

<img width="1909" height="946" alt="image" src="https://github.com/user-attachments/assets/ee9ad1ef-7829-46d4-ba66-3e01670c87b8" />


## 🧩 What it does

- Users submit a **hash (SHA-256)** of their data to the blockchain.
- The smart contract stores the hash along with the **ledger timestamp**.
- Anyone can later verify:
  - Whether the data existed
  - When it was recorded

This ensures **data integrity**, **ownership proof**, and **tamper resistance**.

---

## ✨ Features

- 🔐 **Immutable Proof Storage**
  - Once stored, data cannot be altered.

- ⏱️ **Timestamping**
  - Automatically records the ledger time when proof is stored.

- ✅ **Verification**
  - Easily check if a document hash exists on-chain.

- 📂 **Privacy-Friendly**
  - Only hashes are stored, not actual data.

- ⚡ **Low Cost & Fast**
  - Built on Stellar’s efficient Soroban platform.

---

## 🛠️ Functions

### `store_proof(hash: BytesN<32>)`
Stores the hash of a document with the current timestamp.

### `verify_proof(hash: BytesN<32>) -> bool`
Checks whether a given hash exists in storage.

### `get_proof(hash: BytesN<32>) -> u64`
Returns the timestamp when the hash was stored.

---

## 🌐 Deployed Smart Contract Link

 https://stellar.expert/explorer/testnet/contract/CCZMHC3UCYI3KEQFXPK2PE242QEJHMR4DLHLVWHQMX5SNWSR7UL4S72F

---

## 🧪 Example Use Case

1. Take your document  
2. Generate SHA-256 hash  
3. Call `store_proof(hash)`  
4. Later, verify using `verify_proof(hash)`  

---

## 🔮 Future Improvements

- Add **owner identity (wallet address)**
- Support **metadata storage**
- Add **event logging**
- Enable **multi-file batch proofs**

---

## 📦 Tech Stack

- Soroban SDK (Rust)
- Stellar Blockchain

---

## 👩‍💻 Author

Your Name
