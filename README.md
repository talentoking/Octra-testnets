# Octra Public Testnet

![testnet](https://github.com/user-attachments/assets/aa4f05f1-0f0a-41d0-8ed8-df215b340c46)

## Join Discord
https://discord.gg/octra

---

## Requirements for Codespace
*  use [Github Codespace](https://github.com/codespaces), create a blank template and run your codes.

---

## Install dependecies
Install & Update Packages:
```
sudo apt update && sudo apt upgrade -y
sudo apt install screen curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y
```


---

## Create wallet
### 1. Clone the repository
   ```bash
   git clone https://github.com/0xmoei/wallet-gen.git
   cd wallet-gen
   ```

    ```

### 4. Generate wallet
* Click "GENERATE NEW WALLET" and watch the real-time progress
* Save all the details of your Wallet

---

## Get Faucet
* Visit [Faucet page](https://faucet.octra.network/)
* Enter your address starting with `oct...` to get faucet

![image](https://github.com/user-attachments/assets/18597b40-eaad-434f-a026-cc4a56a6d1a8)

---

## Configure Octra CLI and Wallet

**1. Install Python**
```bash
sudo apt install python3 python3-pip python3-venv python3-dev -y
```

**2. Install CLI**
```bash
git clone https://github.com/octra-labs/octra_pre_client.git
cd octra_pre_client

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

cp wallet.json.example wallet.json
```

**3. Add wallet to CLI**
```bash
nano wallet.json
```
* Replace following values:
  * `private-key-here`: Privatekey with `B64` format
  * `octxxxxxxxx...`: Octra address starting with `oct...`


**4. Run CLI**
```bash
python3 -m venv venv
source venv/bin/activate
python3 cli.py
```
* This should open a Testnet UI

![image](https://github.com/user-attachments/assets/0ba1d536-4048-4899-a977-4517b2e522cd)

---

## Update CLI
After each new task, existing users must update their CLI

### Option A: Normal Update
Update git:
```bash
cd octra_pre_client
git pull origin main
```
* If you see an error about uncommitted changes (e.g., in `cli.py` or other files), stash your changes:
```bash
git stash
git pull origin main
```

Install requirements:
```
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Option B: Wipe and Reclone (Use if Option A fails or you want a clean setup)
Update git:

* Preserve your `wallet.json` file, wipe the repository, and reclone it:
```
mv $HOME/octra_pre_client/wallet.json $HOME/wallet.json
cd && rm -rf octra_pre_client && git clone https://github.com/octra-labs/octra_pre_client.git
mv $HOME/wallet.json $HOME/octra_pre_client/wallet.json
cd octra_pre_client
```

Install requirements:
```
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
---

## Testnet Tasks

## Run CLI
```bash
cd octra_pre_client
python3 -m venv venv
source venv/bin/activate
python3 cli.py
```

## Send transactions
* 1- Encrypt balance
* 2- Send private transaction to another address
  * You can send private transactions to my address: `oct37PG3sZgUZ11LXPxA942MmJaYQaJFAuWDvccVRTi7nT5`
  * Use [Octra Explorer](https://octrascan.io/) to find more octra addresses
* 3- Decrypt balance

---

## Wait for next steps
Stay tuned.
