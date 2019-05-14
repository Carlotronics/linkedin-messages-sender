# linkedin-messages-sender

## Première installation
Assurez-vous d'avoir NodeJS et NPM installés sur votre ordinateur, puis exécutez la commande `npm install` pour télécharger les dépendances du projet.

## Utilisation
 - Créer un fichier Excel `Recipients.xlsx` contenant une colonne `firstname`, `lastname`, `message` et `pj` (toute autre colonne sera ignorée)
 - Exécuter la commande `npm start`, renseignez le temps (en millisecondes) que devra attendre le programme entre chaque envoi de message, puis patientez jusqu'à la fin du programme.

## Fonctionnement
Le script lit le fichier `Recipients.xlsx` et récupère les colonnes nommées `firstname`, `lastname`, `message` et `pj`.
Son fonctionnement est ensuite le suivant, pour chaque ligne après l'en-tête :
 - Chercher le nom du contact dans la page messages privés
 - Sélectionner le contact, remplir le champ message avec le message renseigné dans le fichier excel, et envoyer le message
 - [PAS ENCORE IMPLEMENTE] Si la case `pj` n'est pas vide, envoyer tous les fichiers du dossier pj/ (s'il existe) en pièce(s) jointe(s).