# datactivist website


## Instructions déploiement

1 - faites un fork de https://github.com/Peh4/datactivist-website

2 - dans un terminal
>cd ~
>git clone https://github.com/datactivist/datactivist-website
>cd datactivist-website/hugo/

> hugo server

3 - modifier les fichiers markdown dans les dossiers
> /content/français/homepage
> /content/français/a-propos

4 -Press Ctrl+C to kill the server
> rm -rf public to completely remove the public directory

5 - Faire submodule
>git submodule add -b master git@github.com:datactivist/datactivist.github.io.git public

6 - taper la commande
>hugo

7 - On commit le dossier /public dans le submodule datactivist.github.io
Go To Public folder
> cd public

Add changes to git.
>git add .

>git commit -m "MESSAGE DE COMMIT"

8-
git push origin master

9 - cd ..

10 -
> git add .

> git commit -m "MESSAGE DE COMMIT"

11 - faire un commit du md des pages
> cd ..

> git add .

> git commit -m "MESSAGE DE COMMIT"
