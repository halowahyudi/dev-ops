## Installation Guides

### PHP
[How to Install or Upgrade to PHP 8.3 on Debian/Ubuntu](https://php.watch/articles/php-8.3-install-upgrade-on-debian-ubuntu)

# PHP Laravel Extentions (MOD PHP)
```bash
sudo apt install php8.3-opcache php8.3-pdo php8.3-curl php8.3-intl php8.3-mbstring php8.3-xml php8.3-sqlite3 php8.3-bcmath
```
# PHP Laravel Extentions (PHP-FPM)
```bash
sudo apt install php8.3-fpm php8.3-opcache php8.3-pdo php8.3-curl php8.3-intl php8.3-mbstring php8.3-xml php8.3-sqlite3 php8.3-bcmath

```
### Composer
[How to Install and Use Composer on Ubuntu 22.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-composer-on-ubuntu-22-04)

### Nginx
[How to Install Nginx on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-20-04)

### Node & NPM
[NodeSource Distributions](https://github.com/nodesource/distributions)

### MySQL
[How to Install MySQL on Ubuntu 22.04](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-22-04)

# Membuat Pengguna MySQL dan Memberikan Hak Akses

Untuk membuat pengguna baru `psiswa` dan memberikan hak akses penuh pada semua basis data, ikuti langkah-langkah berikut:

## 1. Masuk ke MySQL sebagai Root

Jalankan perintah berikut di terminal atau command prompt:
```bash
mysql -u root -p
```

Masukkan password root Anda saat diminta.

## 2. Buat Pengguna Baru

Jalankan perintah SQL berikut untuk membuat pengguna baru `psiswa` dan memberikan hak akses:
```bash
CREATE USER 'psiswa'@'localhost' IDENTIFIED BY 'xxx';
```

Gantilah `'xxx'` dengan password yang diinginkan.

## 3. Berikan Hak Akses Penuh

Berikan hak akses penuh pada semua basis data untuk pengguna `psiswa`:
```bash
GRANT ALL PRIVILEGES ON *.* TO 'psiswa'@'localhost' WITH GRANT OPTION;
```

## 4. Segarkan Hak Akses

Segarkan hak akses untuk memastikan perubahan berlaku:
```bash
FLUSH PRIVILEGES;
```

## 5. (Opsional) Ubah Password Pengguna

Jika Anda ingin mengubah password untuk pengguna `psiswa`, Anda dapat menggunakan perintah `ALTER USER`:
```bash
ALTER USER 'psiswa'@'localhost' IDENTIFIED BY 'xxx';
```

Gantilah `'xxx'` dengan password yang diinginkan.

## 6. Keluar dari MySQL

Jika sudah selesai, keluar dari sesi MySQL:
```bash
EXIT;
```

Dengan langkah-langkah di atas, pengguna baru `psiswa` akan memiliki hak akses penuh dan dapat menggunakan password yang telah Anda tentukan. Pastikan untuk mengganti `'xxx'` dengan password yang aman dan sesuai dengan kebijakan keamanan Anda.

