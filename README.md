DNS сервер на BIND9, был сделан в образовательных целях.

## Установка
```bash
# Скопируйте конфиги в нужные директории
sudo cp configs/named.conf /etc/named.conf
sudo cp configs/lab.local.zone /var/named/

# Настройте права
sudo chown named:named /var/named/lab.local.zone
sudo chmod 640 /var/named/lab.local.zone

# Перезапустите BIND
sudo systemctl restart named
