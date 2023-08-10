# Panduan Instalasi dan Konfigurasi Sertifikat SSL/TLS dengan Nginx

## Instalasi Nginx

Jika Anda belum memiliki Nginx terpasang, Anda dapat menginstalnya menggunakan perintah berikut:
```bash
sudo apt update
sudo apt install nginx
```

## Instalasi Certbot

```bash
sudo apt install certbot python3-certbot-nginx
```

## Konfigurasi Sertifikat SSL/TLS dengan Nginx
```bash
sudo certbot --nginx -d domainkamu.com
```

## Pengalihan HTTP ke HTTPS (opsional)
```bash
sudo nano /etc/nginx/sites-available/domainkamu.com
```
- Dalam blok "server" untuk domain Anda, tambahkan baris-baris berikut untuk mengonfigurasi pengalihan:

```nginx
server {
    listen 80;
    server_name seu_dominio.com;
    return 301 https://$host$request_uri;
}
```

## Memperbarui Konfigurasi Nginx
```bash
sudo systemctl reload nginx
```

## Verifikasi dan Pembaruan Otomatis
```bash
sudo certbot renew --dry-run
```
