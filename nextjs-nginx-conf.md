```conf
server {
    listen 80;
    server_name namasitusanda.com www.namasitusanda.com;

    location / {
        proxy_pass http://localhost:3000;  # Sesuaikan port Next.js Anda
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }

    location ~* \.(?:ico|css|js|gif|jpe?g|png)$ {
        expires max;
        add_header Pragma public;
        add_header Cache-Control "public, max-age=31536000";
    }
}

```
