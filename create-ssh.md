# Buat SSH Key
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com" -f ~/.ssh/github_rsa
```
- Lihat Public Key
```bash
cat ~/.ssh/github_rsa.pub
```
- Tambahkan ke Authorized_keys
```bash
cat ~/.ssh/github_rsa.pub >> ~/.ssh/authorized_keys
```

# Github
Mengonfigurasi SSH untuk Menggunakan Kunci Khusus
```bash
nano ~/.ssh/config
```

```bash
Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/github_rsa

```
Uji Koneksi
```bash
ssh -T git@github.com
```
