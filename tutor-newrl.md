<p style="font-size:14px" align="right">
<a href="https://t.me/PemulungAirdropID" target="_blank">Join our telegram <img src="https://user-images.githubusercontent.com/72949170/194228482-0f875615-e155-4b12-8716-8111addd6cba.jpg" width="30"/></a>
</p>

<p align="center">
  <img height="100" height="auto" src="https://user-images.githubusercontent.com/72949170/194707517-88db6e76-1ccb-4021-bdce-493395f13dd9.png">
</p>

# Tutorial NEWRL TESTNET | Node


Dokumen Official :
> [Running Node](https://docs.inery.io/docs/create-token-3](https://docs.newrl.net/Validating/running-validator-node/)

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
<a href="github.com/muhamadramadhani/](https://github.com/muhamad-ramadhani/inery/blob/main/master-node.md" target="_blank">Cara Install Python 3.9 Lengkap</a>
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
