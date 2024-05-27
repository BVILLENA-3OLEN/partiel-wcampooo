# Sujet B

* 👤 Attribué à : `Anthony G` / `Anthony M` / `Arnaud` / `Florian`.

**Rappel** : Les éléments indiqués par le symbole 🚀 sont des éléments « pour aller plus loin » et qui permettront
d'accéder à une note supérieure au partiel.

## ☑️ Mise en place du partiel

1. Indiquez votre nom dans le [`README.md`](../README.md) (début du fichier).
2. Supprimez les fichiers des autres sujets (A / C / D).
3. Lancez le projet et accédez à la page principale pour vérifier que le projet est bien lancé.
4. Faites un **commit**, puis un **push**.
5. **Faites des commits réguliers pour montrer votre progression.**

## 📜 Contexte

Il vous a été demandé de mettre en place une solution de suivi des tâches pour les équipes de développement de votre
entreprise. Les membres de l'équipe pourront suivre les tâches du projet

## 🗃️ Modèles de données

Vous êtes libre de définir le schéma de données qui vous semble le plus adapté au besoin.

Voici quelques précisions liées au métier :

* L'entreprise définit des projets rattachés à des clients.
* Un projet est lié à une application.
  - 🚀 Un projet pourrait être lié à plusieurs applications (API / Front / Mobile / etc.).
  - 🚀 On pourrait définir l'URL du dépôt Git de l'application.
* Au sein d'un projet, le·a chef·fe de projet définit des tâches administratives avec un provisionnement en heures.
* Une tâche de développement est forcément rattachée à une tâche administrative.
  - Se définit par un titre, une description, un état, une affectation, une estimation en heures
    et une consommation en heures.
  - L'état de la tâche peut être : "à faire", "en cours", "à tester", "terminée".
  - 🚀 On pourrait définir le nom de la branche Git associée à la tâche.

## 👔 Règles de gestion

* Les tâches administratives et les tâches de développement sont rattachées à un projet.
* Les tâches ne peuvent pas être supprimées dès qu'il y a eu une consommation en heures.
* Dès qu'un développeur s'affecte une tâche, un e-mail est envoyé au chef de projet.
* Pour passer une tâche à un autre état, il faut indiquer le nombre d'heures consommées.
  - Sauf si l'état initial est "à faire".
  - 🚀 Il pourrait être possible de définir le nombre d'heures consommées au fil de l'eau avec un commentaire.
  - Si la consommation en heures est supérieure à l'estimation, un e-mail est envoyé au chef de projet.
* 🚀 Un tableau de bord permet de suivre les tâches :
  - La consommation en heures par rapport à l'estimation.
  - Les tâches "en cours" et "à tester" par développeur.

## 🛂 Droits d'accès

Il faut forcément se connecter à l'application pour accéder à tous ces détails.

Seuls les membres de l'équipe projet (développeurs, testeurs, chefs de projet, etc.) ont accès aux tâches du projet.

Les comptes des chefs de projet ont les droits d'administration pour gérer les tâches administratives et de
développement.

Les comptes des développeurs ont les droits d'administration sur les tâches de développement.

## 💄 Style

Contentez-vous du minimum pour le style. Vous pouvez le travailler un peu, ce qui pourrait vous donner un bonus, mais
ne perdez pas trop de temps à ce sujet.

## 🤡 Fixtures

Des données *fixtures* seront appréciées.
