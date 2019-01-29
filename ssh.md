# ssh

#### Vérifier que le ssh-agent est actif
```eval $(ssh-agent -s)```

#### Ajouter un clé privée à l'agent ssh
```ssh-add ~/.ssh/other_id_rsa```	

#### Lancer le ssh agent
```eval `ssh-agent -s````
