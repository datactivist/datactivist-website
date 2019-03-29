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

4 - Press Ctrl+C to kill the server, then remove the `public` folder
```sh
git rm -r public
```

5 - Faire submodule
```sh
git submodule add -b master git@github.com:datactivist/datactivist.github.io.git public
```

6 - taper la commande
```sh
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
```

10 -
```sh
git add .
git commit -m "MESSAGE DE COMMIT"
```

11 - faire un commit du md des pages
```sh
cd ..
git add .
git commit -m "MESSAGE DE COMMIT"
```
