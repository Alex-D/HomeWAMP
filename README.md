HomeWAMP
========

## Qu'est-ce que c'est ?
HomeWAMP est une home de substitution à celle d'origine. Un peu plus jolie et plus complète, entre autres. Un atout par rapport à d'autres pages que vous pourrez trouver : elle reste "one-file", telle l'`index.php` d'origine.

Au final, ça ressemble à ça :
![Screenshot de HomeWAMP](https://raw.github.com/Alex-D/HomeWAMP/master/screenshot.jpg "Screenshot de HomeWAMP")

## Installation
1. Renommez votre `index.php` en `index.old.php`, de façon à avoir un backup si besoin
2. Placez simplement le fichier index.php dans votre dossier `www`
3. Admirez et profitez !

## Quoi de neuf ?
Une des choses que j'ai voulu mettre en avant est la possibilité de passer WAMP online sans pour autant montrer tous les détails techniques.
Ainsi, si vous souhaitez montrer un projet indev à votre client, il ne verra pas tout un tas de chose incompréhensibles mais quelque chose de sympathique et de visuellement plus commun.

## Administration
Il y a une page nommée "Administration" accessible depuis l'onglet en haut à droite qui vous permet d'accéder à la configuration du serveur, versions, alias et vous pouvez en rajouter à votre guise en éditant le code.
Il y a entre autres, un bouton pour switcher entre online et offline (plus besoin de passer par l'icône WAMP, pratique pour couper l'accès depuis ailleurs).

## Liste blanche d'administrateurs
Vous trouverez une liste blanche d'IP pour l'accès à l'admin en début de fichier dans une variable `$admin_ip`

## Screenshots & favicon
Pour voir un screenshot de votre site, ajoutez simplement un fichier `screenshot.jpg` dans le dossier du projet. Les dimentions recommandées sont `150x100px`.
En ce qui concerne les favicons, HomeWAMP recherchera de lui-même s'il existe un `favicon.ico` ou `favicon.png` à la racine ou dans `/web/` pour les projets Symfony2.

Note aux développeurs CakePHP, [il faut bypasser la redirection du screenshot pour que ça fonctionne correctement](https://github.com/Alex-D/HomeWAMP/issues/3), comme ceci :

    RewriteEngine on
    RewriteRule ^$ app/webroot/ [L]
    RewriteCond %{REQUEST_FILENAME} !screenshot.jpg
    RewriteRule (.*) app/webroot/$1 [L]

## Auteur
Cette homepage pour WAMP a été créée par (et à la base pour) moi, n'hésitez pas à y contribuer. Vous pouvez me retrouver sur mon site personnel : http://alex-d.fr/

-------

## Aller plus loin
Vous pouvez changer la navigation dans les dossiers par défaut d'apache par celle-ci : http://larsjung.de/h5ai/ qui rajoute un peu d'esthétique en rajoutant, entre autre, un arbre à gauche et un fil d'Arianne en haut.
