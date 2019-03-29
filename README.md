# datactivist website


## Instructions déploiement

1 - faites un fork de https://github.com/Peh4/datactivist-website

2 - dans un terminal
```sh
cd ~
git clone https://github.com/datactivist/datactivist-website
cd datactivist-website/hugo/

hugo server
```

3 - modifier les fichiers markdown dans les dossiers
`/content/français/homepage`, `/content/français/a-propos` etc.

4 - Press Ctrl+C to kill the server, then remove the `public` folder and submodule
```sh
cd ..
rm -rf .git/modules/hugo/public/
# edit .git/config (ex: emacs .git/config)
# delete [submodule "hugo/public"] and its daughters
rm -rf .gitmodules
git rm -r --cached hugo/public
rm -rf hugo/public
```

5 - Ajouter en submodule
```sh
git submodule add -b master git@github.com:datactivist/datactivist.github.io.git hugo/public
```

6 - taper la commande
```sh
cd hugo
hugo
```

7 - On commit le dossier `public/` dans le submodule `datactivist.github.io`
```sh
# go to public folder
cd public
# add changes to git and commit
git add .
git commit -m "MESSAGE DE COMMIT"
```

8-
```sh
git push origin master
```

9 -
```sh
cd ..
git add .
git commit -m "MESSAGE DE COMMIT"
```

10 - faire un commit du md des pages
```sh
cd ..
git add .
git commit -m "MESSAGE DE COMMIT"
git push
```
