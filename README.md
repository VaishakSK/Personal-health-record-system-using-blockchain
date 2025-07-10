# ✅ **Personal Health Records Management Using Blockchain**

> A decentralized framework to securely manage Electronic Health Records (EHR) using blockchain technology and off-chain storage for scalability.

---

## 🚀 **Project Overview**

This framework implements a blockchain-based Electronic Health Records (EHR) system. It offers:

* Granular access control for patients and healthcare providers
* Secure and tamper-proof record storage
* Scalability via off-chain data storage (using IPFS)

The system leverages:

* **Ethereum Smart Contracts** for access control
* **IPFS** for decentralized storage
* **Metamask** for blockchain interaction
* **Ganache** for local blockchain testing

---

## 📦 **Installation Prerequisites**

Ensure you have the following installed:

| Tool         | Purpose                                                 |
| ------------ | ------------------------------------------------------- |
| **Node.js**  | JavaScript runtime for the dApp                         |
| **npm**      | Package manager for Node.js                             |
| **Ganache**  | Local Ethereum blockchain                               |
| **IPFS**     | Decentralized storage                                   |
| **Metamask** | Browser extension for wallet and blockchain interaction |

---

## 🛠️ **Setup Instructions**

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO
```

---

### 2. Install Node Modules

Install dependencies for the dApp:

```bash
npm install
```

---

### 3. Install Ganache

* Download Ganache from [Ganache homepage](https://truffleframework.com/ganache).
* For Linux:

  * You’ll receive an `.appimage` file.
  * Follow [these installation steps](https://itsfoss.com/use-appimage-linux/).

---

### 4. Install IPFS Desktop

* Download from the [IPFS GitHub page](https://github.com/ipfs/ipfs-desktop).
* Install according to your OS instructions.

---

### 5. Install Lite Server

For running the local dApp:

```bash
npm install -g lite-server
```

---

### 6. Install Metamask Extension

* Add Metamask to your browser from [Metamask.io](http://metamask.io/).
* Available for:

  * Google Chrome
  * Firefox
  * Brave Browser

---

## ⚙️ **Configuration Details**

### ✅ Ganache

1. Open Ganache.
2. Click on **Settings**:

   * **Server** tab:

     * Hostname: `127.0.0.1`
     * Port: `8545`
     * Enable Automine
   * **Accounts & Keys** tab:

     * Enable Autogenerate HD Mnemonic

---

### ✅ IPFS Configuration

Run the following commands in your terminal:

```bash
ipfs init
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '["*"]'
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Credentials '["true"]'
ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods '["PUT", "POST", "GET"]'
```

> ⚠️ **Windows Note:**
> Use Command Prompt, Git Bash, or PowerShell if you encounter syntax errors.

---

### ✅ Metamask

* Install the extension.
* Click **TRY IT NOW** if prompted for the new version.
* Accept terms and conditions.
* Stop at the password creation screen for now. You’ll import accounts after deploying the contract.

---

## ✨ **Smart Contract Deployment**

### 1. Install Truffle

```bash
npm install -g truffle
```

---

### 2. Compile Contracts

```bash
truffle compile
```

---

### 3. Start Ganache

* Open Ganache and ensure settings match those above.

---

### 4. Deploy Contracts

```bash
truffle migrate
```

* Copy the deployed contract address and update it in `src/app.js`:

```js
// app/src/app.js  (Line 11)
var agentContractAddress = '0x75E115394aacC7c6063E593B9292CB9417E4cbeC';
```

* If you modify contracts, redeploy:

```bash
truffle migrate --reset
```

> **Note:**
> Resetting changes the contract address. Update `src/app.js` each time.

---

## 🌐 **Running the dApp Locally**

### 1. Connect Metamask to Local Blockchain

* Connect Metamask to `localhost:8545`.
* Click **Import Account**.
* In Ganache, copy a private key from any account and paste it into Metamask to import the account.

---

### 2. Start IPFS Desktop

Launch the IPFS Desktop application.

---

### 3. Launch the Local Server

Navigate to the app directory and start the server:

```bash
cd /YOUR_PROJECT_DIRECTORY/app
npm start
```

Visit:

```
http://localhost:3000
```

🎉 **Your dApp is live locally!**

---

## 🖼️ **Screenshots**

Example contract deployment:

![Ganache Contract Screenshot](images\con-g1.png)

Metamask Connection:

![Metamask Screenshot](images\meta-1.png)

Ganache Account Import:

![Ganache Account Import](images\ganace-contracct.png)

---

## 💡 **Troubleshooting Tips**

* **IPFS command errors (Windows):**
  Try Git Bash or PowerShell with proper escape sequences.

* **Contracts not deploying:**
  Ensure Ganache is running and using the correct network settings.

* **Metamask connection issues:**
  Confirm Metamask is pointing to `localhost:8545`.

---

## 📚 **References**

* [Metamask Official Website](https://metamask.io/)
* [Truffle Suite Documentation](https://trufflesuite.com/docs/)
* [Ganache Documentation](https://trufflesuite.com/ganache/)
* [IPFS Documentation](https://docs.ipfs.io/)

---

## 🔒 **License**

This project is intended for research and educational purposes. Ensure compliance with local data protection laws and blockchain regulations.

---

✨ **Happy coding and stay secure!** ✨
