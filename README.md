# cc-miner ARMbian

Tahapan Install dan Konfigurasi Verus Mining


1. Update dan Upgrade Armbian

```
sudo apt update
sudo apt upgrade
```

2.  Ketik Perintah script dibawah :

```
apt install software-properties-common
```
```
apt-get install libcurl4-openssl-dev libssl-dev libjansson-dev automake autotools-dev build-essential
```
```
apt install git
```
```
git clone --single-branch -b ARM https://github.com/monkins1010/ccminer.git
```
```
cd ccminer
```
```
chmod +x build.sh
chmod +x configure.sh
chmod +x autogen.sh 
```
```
./build.sh 
```

3. Jalankan perintah Autorun Miner dengan Ketik perintah-perintah dibawah :

```
nano mn.sh
```
```
/root/ccminer/ccminer -a verus  -o stratum+tcp://eu.luckpool.net:3956  -u  RNf9CxKM5SttNTBz2QgYu8kJ8djZgPvpsk.STB1  -p x  -t 4 "Jangan Lupa ubah Wallet Addressnya"
```

4. Lanjut ke perintah berikut

```
crontab -e
```
```
@reboot bash /root/ccminer/mn.sh > /root/ccminer/miner.log 2>&1
```



5. Memindahkan Boot ke ROM STB

```
sudo ./install-aml.sh
```
