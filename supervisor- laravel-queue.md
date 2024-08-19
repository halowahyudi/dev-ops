```bash
sudo apt-get install supervisor
```

## Konfigurasi Supervisor (Laravel Queue)
```ini
[program:laravel-worker]
process_name=%(program_name)s_%(process_num)02d
command=php /var/www/path/artisan queue:work --tries=3
autostart=true
autorestart=true
numprocs=3
redirect_stderr=true
stdout_logfile=/var/www/path/storage/logs/worker.log
```
## Realod Supervisor
```bash
sudo supervisorctl reread
sudo supervisorctl update
sudo supervisorctl start laravel-worker:*
```
