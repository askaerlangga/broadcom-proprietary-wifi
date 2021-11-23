# Dokumentasi Install Broadcom proprietary Wifi driver di Debian

Tested on:
- Debian 11 (Bullseye)
- Broadcom BCM4313


Aktifkan repositori `non-free` di `/etc/apt/sources.list`
```sh
sudo nano /etc/apt/sources.list
```
Contoh :

![sources.list](https://github.com/askaerlangga/broadcom-proprietary-wifi/blob/main/Screenshot_2021-11-23_17-41-31.png?raw=true)

Simpan, lalu jalankan perintah :
```sh
sudo apt update
sudo apt install broadcom-sta*
sudo modprobe wl
echo "wl" | sudo tee -a /etc/modules
```
Restart
