# git

#### Git init
```bash
git config --global user.email "gautierjeremy@gmail.com"

git config --global user.name "Jérémy"
```

#### Modifier un fichier en mode global
```bash
git config --global filter.ignoreKey.clean "sed 's/\(key=\).*/\1/g'"
```

#### .gitattributes
```bash
*.file filter=ignoreKey
```
