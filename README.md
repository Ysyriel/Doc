# ProjetReseau
2019
Pierre Caulet, Martin Kyndt, Baptiste Demurger & Guillaume Vanel

La documentation de ce projet est disponible en ouvrant le fichier index.html disponible sous build/html/

## Manuel d'utilisation

Dans une console, entrez:
`python3 serverMultiprocessusComplet.py <numéro de port>`

`<numéro de port>` est le numéro de port qui sera écouté par le serveur (par défaut, 8888)


Sur une autre machine, lancez le client:
`python3 ClientThread.py <adresse IP> <numéro de port>`

`<adresse IP>` est l'adresse du serveur.

`<numéro de port>` doit être identique au numéro de port entré pour lancer le serveur.

**Ces arguments n'ont pas de valeur par défaut, le client s'arrête immédiatement s'ils ne sont pas entrés.**

Votre identifiant vous est demandé, entrez le, puis entrez votre mot de passe. 
Si vous ne vous êtes jamais connecté, entrez un identifiant, il vous sera utile pour des connexions ultérieures. Un mot de passe vous est ensuite demandé pour créer votre compte.

Vous êtes prêts à communiquer avec les autres utilisateurs dès que vous voyez s'afficher le message "vous êtes connecté en tant que: `<identifiant>`", suivi de l'historique des messages échangés. Il vous suffit de taper un message et presser entrer pour l'envoyer. Les messages des autres utilisateurs seront affichés au fur et à mesure de leur réception.

Pour vous déconnecter, pressez simplement ctrl+C, ou tapez !FIN.

Pour fermer le serveur, pressez ctrl+C dans la console qui a servi à le lancer.

Bonne utilisation!

## Tests

Suivez la procédure décrite ci-dessus, en créant votre compte.
Sur une troisème machine, lancez un client et connectez vous avec l'identifiant "test" et le mot de passe "essai". Vous devez voir un message "mot de passe incorrect". Saisissez alors le mot de passe "test". Vous devez être connecté, et ne voir s'afficher l'historique que depuis le dernier message saisi par l'utilisateur "test". 

Échangez quelques messages entre les deux machines, vous pouvez ajouter un troisième client pour vérifier que tout fonctionne.

Déconnectez un utilisateur (ctrl+C). Les autres doivent encore pouvoir échanger des messages (s'il ne reste qu'un utilisateur, vous pouvez voir sur la console du serveur que ses messages sont bien reçus et retransmis à tout le monde sauf lui, donc... à personne).

Reconnectez un des utilisateurs déconnecté (relancez un client et saisissez ses identifiants). Il doit pouvoir communiquer avec les utilisateurs encore présents.


