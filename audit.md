#audit

#### Somes links
[splunking-the-linux-audit-system](https://www.function1.com/2015/07/splunking-the-linux-audit-system)
[sec-understanding_audit_log_files](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/security_guide/sec-understanding_audit_log_files)

#### Configuration de /etc/audit/rules.d/audit.rules à ajouter tel quel dans le 
```-a exit,always  -F dir=/home/splunk/splunk/etc/apps -F perm=warx -F key=splunk_apps_changes```
```-w /etc/rsyslog.conf -p wa -k rsyslog_changes```

