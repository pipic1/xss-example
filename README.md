# xss-example

### Git clone this repo & use Mozilla Firefox

Intro :
Faire php -S localhost:8080 dans le dossier xss-example

Le TP est composé de différentes pages avec un niveau de protection qui augmente au fûr et à mesure.
Rappel : une faille xss consiste à utiliser par exemple du javascript dans un champs pour qu'il soit exécuté par le client.
Le code source PHP est disponible dans le dossier précédement téléchargé.
	-> impossible-level.php empêche tout type de xss.

1) easy-level.php 
	Aucune protection sur la page, vous allez pouvoir faire ce que vous voulez

2) easy-level-2.php
	Une seule petite protection sur la page

3) medium-level.php
	Une protection est faite côté serveur.

4) bank-level.php ( couplage CSRF )
	On considère que la banque effectue ses transferts grâce aux requêtes GET.
	
	La requête est composée de 2 paramètres : amount( montant du transfert ) & to ( id de l'user, normalement le votre)

	- Utiliser alert('Vous êtes bien connecté à votre compte')
	- Utiliser window.location.href ( pour rediriger l'utilisateur : CSRF)
	- Aide : le '&' peut aussi s'écrire ...

5) Retourner sur easy-level.php
	Vous allez essayer d'enregistrer un fichier sur le pc d'un utilisateur en utilisant le script FilesSaver.js
	
	Doc : https://github.com/eligrey/FileSaver.js/
	
	CDN : https://fastcdn.org/FileSaver.js/1.1.20151003/FileSaver.min.js ( peut être utile 😉 )

Si vous avez du temps, essayez d'exploiter les failles sur ce site : https://xss-game.appspot.com/
