# Commandes

#### Voir la taille des répertoires triés par ordre croissant
``du -xk ./* | sort -n``

``du -hs * | sort -h``
#### Lancer une commande en root en gardant le path de l'utilisateur actuel
``nohup sudo env "PATH=$PATH" node server.js &``

#### Copier sa clé public sur un serveur distant pour ssh
``cat .ssh/id_rsa.pub | ssh 192.168.1.36 -l pi "cat - >>.ssh/authorized_keys"``

#### Compare le contenu de deux répertoires et montre la différence
``diff -rq dir1 dir2 # compare folder contents and show the difference``

#### Alias dans le fichier .bashrc ou le shell
``alias updateAll='sudo apt-get update && sudo apt-get upgrade'``

#### Export d'une variable dans le .bashrc ou le shell
``export PATH=$PATH:'/home/pi/nodejs/nodejs/bin'``

#### Tuer des processuss à partir de leur nom
``sudo kill $(ps aux |grep -v grep|grep <id-process>|awk -F' ' '{print $2}')``

#### Envoyer un paquet UDP
``echo -n "hello" | nc -4u -q1 localhost 5140``

``echo -n "Nov  9 09:04:18 haproxy-00 dhclient[151]: DHCPACK of 10.10.2.175 from 10.10.2.1" | nc -4u -q1 localhost 5140``

#### Lancer des commandes dans un conteneur
``lxc exec haproxy-00  -- bash -c "ps && ls"``

```JavaScript
REMOTE_SCRIPT="lxc list
lxc exec haproxy-00  -- bash -c \"
cd /opt
ls -al
ps -aux\"
"
```

#### Se logger dans un conteneur
``lxc exec <conteneur-id> bash``

#### Voir les ports ouverts sur une machine
``netstat -tulpn``

#### Désinstaller un paquet proprement
```
apt-get remove rsyslog
apt-get --purge autoremove
dpkg -P rsyslog
```

#### Test de résolution de nom de domaine
```
curl <addr1> --resolve <addr2> # resolve address 1 to address 2. Useful for testing.
```
