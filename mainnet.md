<p style="font-size:14px" align="right">
<a href="https://t.me/PemulungAirdropID" target="_blank">Join our telegram <img src="https://user-images.githubusercontent.com/72949170/194228482-0f875615-e155-4b12-8716-8111addd6cba.jpg" width="30"/></a>
</p>

# NEWRL Mainnet

Official documentation:
>- [Validator setup instructions](https://docs.nibiru.fi/run-nodes/testnet/)

## 1. Stop Node

- Kill dulu
```
cd ~/newrl-venv/newrl
scripts/kill_server.sh
```

simpan file.auth.json di ```~/newrl-venv/newrl/data_testnet```

- Hapus newrl (bisa new tab)
```
cd
rm -rf newrl-venv
```

## 2. Setup Mainnet
- Open Port
```
sudo ufw allow ssh && sudo ufw allow 8456 && sudo ufw enable
```

- Update Packages
```
sudo apt update && sudo apt upgrade -y
```

- Install Pelengkap hidup
```
sudo apt install -y build-essential libssl-dev libffi-dev git curl screen
```
- Install Python 3.9 (jika sudah tak usah)
```
sudo apt install python3.9
```
- Install Pip & Python3 venv
```
curl -sSL https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python3 get-pip.py
sudo apt install python3.9-venv
```
```
sudo mkdir newrl-venv
cd newrl-venv
python3.9 -m venv newrl-venv
```
- Aktivasi
```
source newrl-venv/bin/activate
```

- Download dan run Script
```
git clone https://github.com/newrlfoundation/newrl.git
```
```
cd newrl
scripts/install.sh mainnet
```
- Import Wallet Testnet ke Mainnet
```
cd ~/newrl-venv/newrl/data_mainnet
```
```
nano .auth.json
```
Isi dengan data yang di testnet
Format yang diinput
>{"public": "fefcdb9c187f241ffbe76ef89ee9ff85dcd6a1ba0ad60dedaeb195d4azzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz",
>"private": "be46bf4f061d6a6d813005zzzzzzzzzzzzzzzzzzzzzzzzzzz",
>"address": "0x0000000000000000000000000000000000000DEAD"}

- Cek ulang buat memastikan
```
cd ~/newrl-venv/newrl
python3 scripts/show_wallet.py
```

![image](https://user-images.githubusercontent.com/72949170/199658100-5e04be26-b71d-45ff-91d0-6b178bf8b89f.png)

## 3.Import ke wallet website
- Buka https://wallet.newrl.net/login/
- Login dengan format yang diatas 
- Ubah jadi mainnet

![image](https://user-images.githubusercontent.com/72949170/199658395-acc7720f-321c-4017-b793-714d88949d2e.png)

- Lakukan KYC
- Tunggu sampai approve

![image](https://user-images.githubusercontent.com/72949170/199658576-7ab41884-7f41-4b70-8835-82b0c588e97c.png)

## 4. Jalankan Node
```
screen -S newrl
scripts/start.sh mainnet
```

![image](https://user-images.githubusercontent.com/72949170/199658778-3ec88163-eecf-4637-b86d-75c4cd003d5e.png)

Untuk keluar dari sesi logs tekan ```CTRL+A+D```
Untuk kembali cek logs
```
screen -Rd newrl
```

## 5. Stake OG Token

Setelah mendapat 1 OG Token dan 10 Newrl di wallet mainnet, pergi wallet buka Validator Management

![image](https://user-images.githubusercontent.com/72949170/199658933-a1b4f448-2efd-4e65-b8d2-66f975a26c88.png)

- Klik ```Stake Using My OG Token```
- Cek logs di VPS

![image](https://user-images.githubusercontent.com/72949170/199659101-da923134-6491-4600-b9b3-7ee2d8311455.png)

- Jika sudah begitu berarti done
- Kembali ke wallet dan tunggu sampai Newrl mulai berjalan

![image](https://user-images.githubusercontent.com/72949170/199659138-7d75b4f5-2d8a-484e-ab0b-89b0017807c4.png)


## DONE


