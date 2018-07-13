# Syslog

#### Documentation officielle avec les variables d'entrée
```
[Documentation](http://www.rsyslog.com/doc/v8-stable/configuration/properties.html)
```

#### Traitement des logs
```
$template prod1,"/var/log/prod1/%FROMHOST-IP%/%syslogfacility-text%.log"
$template prod2,"/var/log/prod2/%FROMHOST-IP%/%syslogfacility-text%.log"
if $fromhost-ip=='172.16.111.111' then ?prod1
if $fromhost-ip=='172.16.111.222' then ?prod1
if $fromhost-ip=='172.16.222.111' then ?prod2
```

```
$template DynaFile,"/var/log/%FROMHOST-IP%/%syslogfacility-text%.log"
*.* -?DynaFile
```

```
$umask 0022
$FileCreateMode 0655
$DirCreateMode 0755
```
