# Sujet A

* 👤 Attribué à : `Ahmed` / `Damien` / `Eliott` / `Lenny`.

**Rappel** : Les éléments indiqués par le symbole 🚀 sont des éléments « pour aller plus loin » et qui permettront
d'accéder à une note supérieure au partiel.

## ☑️ Mise en place du partiel

1. Indiquez votre nom dans le [`README.md`](../README.md) (début du fichier).
2. Supprimez les fichiers des autres sujets (B / C / D).
3. Lancez le projet et accédez à la page principale pour vérifier que le projet est bien lancé.
4. Faites un **commit**, puis un **push**.
5. **Faites des commits réguliers pour montrer votre progression.**

## 📜 Contexte

Votre client souhaite une application web pour gérer des événements organisés au sein de ses différentes agences. Ces
événements sont ensuite mis à disposition du personnel de l'agence organisatrice pour qu'ils puissent s'inscrire.

## 🗃️ Modèles de données

Vous êtes libre de définir le schéma de données qui vous semble le plus adapté au besoin.

Voici quelques précisions liées au métier :

* L'entreprise du client possède plusieurs agences en France. Certaines sont dans la même ville ou région.
* Les événements sont organisés par une agence.
  - 🚀 Les événements pourraient être organisés par plusieurs agences, mais une agence demeurera l'organisatrice
       principale. Ces événements sont alors des **événements communautaires**.
* Les événements sont de plusieurs types : afterwork, formation, séminaire, etc.
* Un événement est défini par une date, un lieu et, possiblement, un nombre de places limitées.
  - ⚠️ Un événement peut être défini sur une période.
  - 🚀 Les responsables des agences pourraient avoir des places réservées, qui ne compteraient pas dans la limite des
       places limitées.

## 👔 Règles de gestion

* L'événement ne peut plus être modifié ou supprimé une fois qu'il a débuté.
  - Si la date est modifiée, les personnes inscrites doivent être prévenues par e-mail.
  - Même chose pour le lieu.
* Les inscriptions sont ouvertes jusqu'à la veille de l'événement.
  - 🚀 Une date limite d'inscription pourrait être définie.
* Dès qu'un utilisateur s'inscrit à un événement, il reçoit un e-mail de confirmation.
* 🚀 Dès la création de l'événement, celui-ci est en statut « brouillon » et n'est pas visible par les utilisateurs.
  - Il ne devient visible que lorsque l'agence organisatrice le publie.

## 🛂 Droits d'accès

Il faut forcément se connecter à l'application pour accéder à tous ces détails.

Certains comptes, désignés par l'agence correspondante, ont des droits d'administration pour gérer les événements.

Seuls les événements de sa propre agence sont visibles pour un utilisateur.

## 💄 Style

Contentez-vous du minimum pour le style. Vous pouvez le travailler un peu, ce qui pourrait vous donner un bonus, mais
ne perdez pas trop de temps à ce sujet.

## 🤡 Fixtures

Des données *fixtures* seront appréciées.
