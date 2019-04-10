# datactivist website
Instructions pour pouvoir contribuer du contenu au site.

## Mise en place pour nouveau contributeur

1. Sur GitHub, faire un fork de https://github.com/datactivist/datactivist-website

2. Dans un terminal, cloner le fork et ajouter un lien vers le repo datactivist"upstream":
```sh
cd /path/to/wherever
git clone https://github.com/<your_login>/datactivist-website
git remote add upstream https://github.com/datactivist/datactivist-website
```

Puis pour tenir son fork à jour :
https://help.github.com/en/articles/syncing-a-fork


## Modifier le contenu
1. Dans un terminal:
```sh
cd /path/to/wherever
cd datactivist-website/hugo/

hugo server
```

2. Modifier les fichiers markdown dans les dossiers
`/content/français/homepage`, `/content/français/a-propos` etc.

3. Appuyer sur Ctrl+C pour tuer le serveur

4. Supprimer le dossier `public` et le submodule git correspondant:
```sh
cd ..
rm -rf .git/modules/hugo/public/
# edit .git/config (ex: emacs .git/config)
# delete [submodule "hugo/public"] and its daughters
rm -rf .gitmodules
rm -rf hugo/public
git rm -r --cached hugo/public
```

5 - Ajouter le submodule git:
```sh
git submodule add -b master git@github.com:datactivist/datactivist.github.io.git hugo/public
```

6 - Générer le site statique à partir du contenu:
```sh
cd hugo
hugo
```

7 - Déployer la nouvelle version du site en poussant le contenu du dossier `public/` sur `datactivist.github.io` (via le submodule git):
```sh
# go to public folder
cd public
# add changes to git and commit
git add .
git commit -m "MESSAGE DE COMMIT"
# push changes
git push origin master
```

8 - Committer et pousser les modifs du contenu sur son fork:
```sh
# commit modifs in the folder hugo/ only
cd ..
git add .
git commit -m "MESSAGE DE COMMIT"
# commit modifs in the root folder for datactivist-website
cd ..
git add .
git commit -m "AUTRE MESSAGE DE COMMIT"
# push all modifs
git push
```
