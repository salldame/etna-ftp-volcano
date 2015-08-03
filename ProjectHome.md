TCM-RUBY-001 - VOLCANO FTP


Modalités
Le projet est à faire par groupes de deux (et non des groupes de un).

Aucun autre langage que Ruby pour les scripts sera accepté (ce qui signifique que pour des requêtes de BDD, par exemple, SQL est autorisé)

Le serveur devra absolument fonctionner avec un client FTP (`ftp' en ligne de commande, FileZilla, Transmit, etc.).
Aucun serveur ne sera accepté s'il ne fonctionne qu'avec telnet.


Sujet
Maintenant que vous avez les bases de programmation en Ruby, vous allez devoir mettre ça en oeuvre !
Pour cela, votre projet sera un serveur FTP. Mais un simple serveur FTP ne révelera pas les possiblités de Ruby, c'est pourquoi il va falloir accompagner votre serveur de petits "add-ons"

Les fondations du serveurs sont posées et vous serons fournies. Avec ces fondations, plusieurs clients peuvent se connecter, et une session est créée pour chacun d'eux.
Au minimum, le serveur doit fonctionner avec la ligne de commande ftp, au mieux avec des clients graphiques tels FileZilla, Transmit, etc.
Tout client ne fonctionnant que sous telnet sera refusé. Telnet n'est à utiliser que pour les tests préalables, mais il est vigoureusement conseillé d'utiliser les clients FTP le plus tôt possible.

A côté de ça, il vous sera demandé différents scripts qui pourront interagir avec le serveur, comme simplement le quitter / lancer, ou générer des statistiques.

Partie obligatoire

Serveur FTP qui suit la RFC 959
Commandes suivantes implémentées:
PWD
CWD
QUIT
LIST
STOR
RETR
Fichier de configuration (le YAML est la piste la plus simple)
Les trois paramètres suivants devront pouvoir être renseignés : addresse de bind, port d'écoute, répertoir racine.
Script de démarrage permettant de lancer, quitter, ou relancer le serveur
Votre serveur devra pouvoir être capable d'enregistrer des données statistiques, avec au minimum:
Les connexions (avec la date)
Le nombre de fichiers tranférés par chaque connexion
La durée de chaque connexion
La taille de chaque fichiers transférés (par forcément rattaché à la connexion en cours)
A noter que si le serveur est quitté par le script sus-cité, il faudra tout de même enregistrer les données pour les utilisateurs actuellement connectés
Vous êtes libre du format de stockage (XML, basse de donnée, etc.), mais il est important que le résultat soit exploitable par d'autres scripts potentiels

Pensez à bien vous répartir les tâches. Chaque partie est importante, et notée, donc n'en oubliez pas, ou ne vous arrêtez pas parce qu'une chose vous bloque. Il y a toujours moyen de faire quelque chose, soyez inventifs.

Partie optionnelle (bonus)

Possibilité de quérir le serveur pour savoir exactement combien de personnes sont connectées
Script / Site permettant de visualiser les statistiques générées par le serveur (comme par exemple "moyen de commandes par connexion")
Statistiques ++ (éventuellement visibles sur le site aussi), comme par exemple la vitesse moyenne de chaque téléchargement (et/ou de tous les téléchargements)
N'importe quoi qui utiliserait des fonctions spécifiques à votre système (et qui a un réel intérêt)