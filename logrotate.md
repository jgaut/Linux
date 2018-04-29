#logrotate

#### Fichier exemple : /etc/logrotate.d/firewall
```
/var/log/*.9/*.log {
  rotate 1
  daily
  size 1
  compress
  missingok
  notifempty
}
```

#### Lancement d'une commande logrotate
```
sudo logrotate -f /etc/logrotate.d/firewall
```
