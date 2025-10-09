# 🛡️ MAWARI NETWORK – Guardian Node Setup Guide
- Credits to NTExhaust

### 📘 Official Documentation  
[**Mawari Docs: Guardian Node (Testnet)**](https://docs.mawari.net/decentralized-infrastructure-offering-dio/operating-the-guardian-node-testnet)

---

### 🔗 Useful Links

- **Faucet Hub:** [https://hub.testnet.mawari.net/](https://hub.testnet.mawari.net/)  
- **Video Tutorial:** [YouTube Guide](https://www.youtube.com/watch?v=kFy-SlfkCi4&feature=youtu.be)

### LETS START

### REMEMBER TO USE NEW WALLET - OR ADD NEW WALLET ON YOUR METAMASK

## GET FAUCET HERE:
- [https://hub.testnet.mawari.net/](https://hub.testnet.mawari.net/)

## MINT YOUR NFT - LICENSE 
- Mint 3 NFT
- **Mint Guardian NFT:** [https://testnet.mawari.net/mint](https://testnet.mawari.net/mint)  

<img width="1273" height="974" alt="image" src="https://github.com/user-attachments/assets/4965d3bf-180d-4830-b20c-251a23a6105d" />


---

## 🧩 Requirements
- [Docker](https://docs.docker.com/get-docker/) installed on your system  
- A wallet address (Metamask or other EVM-compatible wallet)

---

## ⚙️ Step-by-Step Setup

### 1️⃣ Create Project Folder
```bash
mkdir -p ~/mawari
cd ~/mawari
```

---

### 2️⃣ Set Node Image Name
```bash
export MNTESTNET_IMAGE=us-east4-docker.pkg.dev/mawarinetwork-dev/mwr-net-d-car-uses4-public-docker-registry-e62e/mawari-node:latest
```

---

### 3️⃣ Set Your Owner Wallet Address  
Replace `0x123abc` with your actual wallet address:
```bash
export OWNER_ADDRESS=0x123abc
```

---

### 4️⃣ Create a Screen Session  
This keeps your node running even if you close the terminal:
```bash
screen -S mawari
```

---

### 5️⃣ Run the Guardian Node
```bash
docker run --pull always -v ~/mawari:/app/cache -e OWNERS_ALLOWLIST=$OWNER_ADDRESS $MNTESTNET_IMAGE
```

---

### 6️⃣ Check Logs & Get Burner Address
Look for the log line that shows:
```
[INFO]  Using burner wallet {"address": "<your burner wallet appears here>"}
```

To find it manually:
```bash
nano $HOME/mawari/flohive-cache.json
```

---

### 7️⃣ Fund Your Burner Wallet  
Send **1 test token** from your main wallet to your **burner wallet address**.

---

### 8️⃣ Activate Guardian Node
Go to: [https://app.testnet.mawari.net/](https://app.testnet.mawari.net/)

Then:
1. Select your all 3 **Guardian IDs**  
2. Click **Delegate**  
3. Enter your **burner address**  
4. Confirm the transaction  
5. ✅ Done — your Guardian Node is live!

---
<img width="1363" height="870" alt="image" src="https://github.com/user-attachments/assets/a7313088-e619-422f-8ad9-d8177f39275b" />

### 📹 Video Tutorial
🎥 [Watch Setup Walkthrough on YouTube](https://www.youtube.com/watch?v=kFy-SlfkCi4&feature=youtu.be)
