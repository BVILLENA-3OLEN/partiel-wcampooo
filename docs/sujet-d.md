# Sujet D

* 👤 Attribué à : `Alexandre` / `Aymane` / `Ayoub` / `Victorio`.

**Rappel** : Les éléments indiqués par le symbole 🚀 sont des éléments « pour aller plus loin » et qui permettront
d'accéder à une note supérieure au partiel.

## ☑️ Mise en place du partiel

1. Indiquez votre nom dans le [`README.md`](../README.md) (début du fichier).
2. Supprimez les fichiers des autres sujets (A / B / C).
3. Lancez le projet et accédez à la page principale pour vérifier que le projet est bien lancé.
4. Faites un **commit**, puis un **push**.
5. **Faites des commits réguliers pour montrer votre progression.**

## 📜 Contexte

Votre entreprise a besoin d'une application web pour suivre les candidatures, qu'elles soient spontanées ou en réponse à
une offre d'emploi.

## 🗃️ Modèles de données

Vous êtes libre de définir le schéma de données qui vous semble le plus adapté au besoin.

Voici quelques précisions liées au métier :

* L'entreprise possède plusieurs services. Chaque service possède plusieurs offres d'emploi. Une offre d'emploi est
  rattachée à un·e manager qui est référent du poste, ainsi qu'à un·e RH qui est en charge du recrutement.
* Les RH sont associés à un ou plusieurs services.
* Une candidature est définie par les informations du candidat, une date de candidature et une offre d'emploi ou un
  poste, pour une candidature spontanée.
  - Une candidature est associée à un statut : en cours, refusée, acceptée.
  - Une candidature indique une liste de choses à faire : réceptionner le CV, définir une date d'entretien,
    faire passer des tests techniques, etc.

## 👔 Règles de gestion

* Lorsqu'une candidature est créée, un e-mail de confirmation est envoyé au candidat et un e-mail de notification est
  envoyé au manager.
  - C'est au RH de créer la candidature, à partir des informations fournies par le·a candidat·e.
* Au fil du processus de recrutement, le RH peut mettre à jour sa liste de choses à faire.
* Une candidature ne peut qu'être archivée ; aucune suppression possible.
* Lorsqu'une candidature est acceptée ou refusée, un e-mail est envoyé au candidat.
  - La candidature est alors archivée.
* 🚀 Une réunion pourrait être organisée par le RH ou par le manager pour discuter de la candidature :
  - Entre RH et candidat·e OU entre manager et candidat·e OU entre RH, manager et candidat·e OU entre RH et manager.
  - D'autres personnes pourraient être invitées à cette réunion.
  - Plusieurs réunions pourraient être organisées pour une même candidature.
  - Les participants recevraient une notification par e-mail.

## 🛂 Droits d'accès

Il faut forcément se connecter à l'application pour accéder à tous ces détails.

Les comptes RH peuvent gérer des dossiers de candidature. La création est possible que pour le ou les services auxquels
ces comptes sont rattachés. La modification et la suppression ne sont possibles que pour leurs propres dossiers.

Les comptes des managers peuvent suivre l'état des candidatures auxquels ces comptes sont rattachés.

## 💄 Style

Contentez-vous du minimum pour le style. Vous pouvez le travailler un peu, ce qui pourrait vous donner un bonus, mais
ne perdez pas trop de temps à ce sujet.

## 🤡 Fixtures

Des données *fixtures* seront appréciées.
