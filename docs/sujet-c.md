# Sujet C

* 👤 Attribué à : `Amélie` / `Augustine` / `Mathys` / `William`.

**Rappel** : Les éléments indiqués par le symbole 🚀 sont des éléments « pour aller plus loin » et qui permettront
d'accéder à une note supérieure au partiel.

## ☑️ Mise en place du partiel

1. Indiquez votre nom dans le [`README.md`](../README.md) (début du fichier).
2. Supprimez les fichiers des autres sujets (A / B / D).
3. Lancez le projet et accédez à la page principale pour vérifier que le projet est bien lancé.
4. Faites un **commit**, puis un **push**.
5. **Faites des commits réguliers pour montrer votre progression.**

## 📜 Contexte

Votre entreprise a besoin d'une application web pour gérer les réservations des salles de réunion au sein de chaque
établissement. Un formulaire permettra de réserver une salle à une date pendant une période temporelle, à condition
qu'elle soit disponible.

## 🗃️ Modèles de données

Vous êtes libre de définir le schéma de données qui vous semble le plus adapté au besoin.

Voici quelques précisions liées au métier :

* L'entreprise possède plusieurs établissements. Chaque établissement possède au moins une salle de réunion.
* Une salle de réunion est définie par un nom, une capacité d'accueil et une localisation dans le bâtiment (le numéro
  d'étage par exemple).
* Une réservation est définie par une date, une heure de début, une heure de fin et, forcément, une salle de réunion.
  - 🚀 Une réunion pourrait être récurrente (tous les lundis, par exemple), sur une période donnée.
  - 🚀 Certains participants pourraient être définis comme des personnes extérieures (formateur·rice, client·e, etc.).
  - 🚀 Une réservation pourrait être prise pour le compte d'une autre personne. L'utilisateur agirait alors en tant que
    délégataire et pourrait ne pas être présent lors de la réunion.

## 👔 Règles de gestion

* Une salle de réunion ne peut pas être réservée si elle est déjà occupée à la date et à l'heure souhaitées.
* Dès qu'une salle est réservée, un e-mail de confirmation est envoyé à la personne ayant effectué la réservation.
* La personne ayant réservé la salle peut ajouter des participants à la réunion.
  - Les personnes invitées reçoivent un e-mail de notification.
  - 🚀 Une personne invitée pourrait indiquer si elle sera présente ou non et en présentiel ou en distanciel.
  - 🚀 Une personne invitée pourrait inviter une autre personne, mais cela doit être validé par la personne ayant
    créé la réunion.
* Seule la personne ayant mis en place la réservation peut la modifier ou la supprimer.
    - Une modification dans la date ou l'heure doit être notifiée par e-mail aux personnes inscrites.
    - Même chose pour une modification sur la salle de réunion.
    - Même chose pour une suppression.
* Une modification ou une suppression peut être effectuée jusqu'à 30 minutes après le début de la réunion.
* 🚀 Un tableau de bord permet de suivre ses réservations :
  - Les réservations du jour.
  - Les réservations de la semaine.
  - Les réservations du mois.

## 🛂 Droits d'accès

Il faut forcément se connecter à l'application pour accéder à tous ces détails.

Il n'est possible de réserver une salle que pour son propre établissement.

Seuls les participants à la réunion peuvent voir les détails de la réservation.

## 💄 Style

Contentez-vous du minimum pour le style. Vous pouvez le travailler un peu, ce qui pourrait vous donner un bonus, mais
ne perdez pas trop de temps à ce sujet.

## 🤡 Fixtures

Des données *fixtures* seront appréciées.
