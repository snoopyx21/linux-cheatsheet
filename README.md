# Useful commands


Check disk space:
```
df -g
```

Check lvm space:
```
df -h
```

Check repository space 
```
du . --max-depth=1 -h
```

Commandes utiles Zabbix
```
firewall-cmd --permanent --add-port=1500/tcp --add-source=<IP>:<PORT>
firewall-cmd --reload

zabbix_agentd -V

su -s /bin/bash zabbix
```

Nettoyer les logs de journalctl
```
journalctl --disk-usage
journalctl --vacuum-time=2d
journalctl --vacuum-size=1G
journalctl --verify
```

Convert CER to CRT
```
openssl x509 -inform PEM -in certificate.cer -out certificate.crt
```

Read information from PEM
```
openssl x509 -text -in cert.pem
```

Scan a host & get all algos used by SSH
```
nmap --script ssh2-enum-algos -sV -p <PORT> <IP>
```

Test sendmail
```
echo "Subject: sendmail test" | sendmail -v <MAIL>
```

Send a command from ansible
```
ansible groupe -a "cmd" -u ansibleadmin --become
```

Capture network traffic
```
tcpdump -i any host <IP> -vvvvv -w /tmp/capture.pcap
```

Trouver un mot dans le repertoire courant
```
yum -y install yum-plugin-versionlock
yum versionlock <PACKAGE>
```

Find a work in the current repo
```
grep -nr '*word*' .
```

Get a file with scp
```
scp -P <PORT> <USERNAME>@<HOSTNAME>:<PATH_DEST> <PATH_SRC>
```

Commandes utiles history
```
history -d <LINE>
History -w
```
