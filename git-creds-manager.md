# Git Creds Manager
- Install Git Creds Manager
```bash
sudo apt-get install libsecret-1-0 libsecret-1-dev
sudo apt-get install git-credential-manager-core
git-credential-manager-core configure
```
- Clone Repo
```bash
git clone https://github.com/nama_pengguna/nama_repo.git
```

## Konfigurasi Git Secara Global
```bash
git config --global user.name "Nama Anda"
git config --global user.email "email@example.com"
```
- Ingat di cache
```bash
git config --global credential.helper cache
```
## Test Pull Request
```bash
git pull origin main # sesuaikan dengan branch
```
Jika sudah tidak ada lagi masukkan username dan personal akses token maka bisa lanjut untuk setup github action.
