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
``sudo kill $(ps aux |grep -v grep|grep crond|awk -F' ' '{print $2}')``
