<p style="font-size:14px" align="right">
<a href="https://t.me/PemulungAirdropID" target="_blank">Join our telegram <img src="https://user-images.githubusercontent.com/72949170/194228482-0f875615-e155-4b12-8716-8111addd6cba.jpg" width="30"/></a>
</p>

<p align="center">
  <img height="100" height="auto" src="https://user-images.githubusercontent.com/72949170/194707517-88db6e76-1ccb-4021-bdce-493395f13dd9.png">
</p>

# Tutorial NEWRL TESTNET | Node


Dokumen Official :
> [Running Node](https://docs.newrl.net/Validating/running-validator-node/)

**LANGSUNG AJA KITA MULAI**

## 1. Setup 
**Open Port**
```
sudo ufw allow ssh && sudo ufw allow 8421 && sudo ufw enable
```
**Update**
```
sudo apt update && sudo apt upgrade
```
**Download Bumbu kehidupan**
```
sudo apt install -y build-essential libssl-dev libffi-dev git curl screen
```
**Install Python**
```
sudo apt install python3.9
```
*Jika saat install python eror, kalian bisa ke sini*
<p>
<a href="https://github.com/muhamad-ramadhani/newrl/blob/main/install_python.md" target="_blank">Cara Install Python 3.9 Lengkap</a>
</p>

**Install Pip dan Python3-venv**

```
curl -sSL https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```

```
sudo apt install python3.9-venv
```

```
sudo mkdir newrl-venv
```

```
cd newrl-venv
```

```
python3.9 -m venv newrl-venv
```

**Didalam directory ```newrl-venv``` jalankan command**
```
source newrl-venv/bin/activate
```

## 2. Install NEWRL
```
git clone https://github.com/newrlfoundation/newrl.git
```

**Jalankan script**
```
cd newrl
```

```
scripts/install.sh testnet
```

## 3. Buat Wallet
```
python3 scripts/show_wallet.py
```
Ketik  ```Testnet```
> Output
> 
> {"public": "fefcdb9c187f241ffbe76ef89ee9ff85dcd6a1ba0ad60dedaeb195d4azzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz", "private": "be46bf4f061d6a6d813005zzzzzzzzzzzzzzzzzzzzzzzzzzz", "address": "0x0000000000000000000000000000000000000DEAD"}

**WAJIB BACKUP**

**Pergi ke https://wallet.newrl.net/**
- Buat Password
- Import Wallet
- Isi dengan output yang tadi
- Isi detail lainnya

## 4. Request Faucet
https://wallet.newrl.net/faucet/


<p align="center">
  <img height="auto" height="auto" src="https://user-images.githubusercontent.com/72949170/194708435-d5ed5bf7-c501-4ac5-83bd-83de0f61a229.png">
</p>


## 5. Run Node
```
screen -S newrl
```

```
scripts/start.sh testnet
```

<p align="center">
  <img height="auto" height="auto" src="https://user-images.githubusercontent.com/72949170/194708533-cf7c2779-760d-43f8-ab2c-f0be44ac5f28.png">
</p>

**Untuk Close screen kalian bisa CTRL+A+D**

## 6. Stake
**Buka Wallet**
**Klik Garis tiga di pojok kiri atas**
**Pilih ``Run a Node``**
**Stake**

<p align="center">
  <img height="auto" height="auto" src="https://user-images.githubusercontent.com/72949170/194708681-db9c26ca-1a41-44be-b08b-87e8259adcff.png">
</p>

## 7. Cek
**Cek riwayat transaksi**
```
http://archive1-testnet1.newrl.net:8421/sc-state?table_name=stake_ledger&contract_address=ct1111111111111111111111111111111111111115&unique_column=wallet_address&unique_value=YOURADDRESS
```
**Cek riwayat mining**
```
http://144.91.99.67:8421/get-incoming-trustscores?dst_wallet_address=YOURADDRESS
```

## DONE
