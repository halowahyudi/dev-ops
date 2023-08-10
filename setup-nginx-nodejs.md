---
title: Setup Server Linux untuk NodeJS
---

# Persiapan Server

- Siapkan server Linux (misalnya Ubuntu) dengan akses root atau sudo.
- Instal Node.js, NPM

# Konfigurasi NGINX
- Install NGINX
```bash
sudo apt install nginx
```
- Mulai Nginx
```bash
sudo systemctl start nginx
```
Aktifkan agar Nginx berjalan saat boot
```bash
sudo systemctl enable nginx
```
# Setup Project
- Buat direktori projek
```bash
mkdir /var/www/namaproject
```
- Buat server blok
```bash
sudo nano /etc/nginx/sites-available/namaproject
```
- Set Hak Akses
```bash
sudo chown -R www-data:www-data /var/www/namasitusanda
```
- Aktifkan Konfigurasi
```bash
sudo ln -s /etc/nginx/sites-available/namaproject /etc/nginx/sites-enabled
```
- Cek apakah konfigurasi sudah benar
```bash
sudo nginx -t
```
- Restart NGINX
```bash
sudo systemctl restart nginx
```

# Aktifkan Firewall
```bash
sudo ufw enable
```
- Cek apakah sudah aktif
```bash
sudo ufw status
sudo ufw status verbose
```
### Buka Port 80, 443
```bash
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
```
