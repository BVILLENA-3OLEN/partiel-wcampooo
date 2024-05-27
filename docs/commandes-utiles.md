# 3OLEN - Framework "Symfony" - Commandes

## 🔔 Rappels

Symfony intègre un composant "console" qui permet d'exécuter des commandes dans un terminal afin d'effectuer diverses
actions :

* Monter / Supprimer / Mettre à jour la base de données et son schéma.
* Générer du code à travers des *makers*.
* Mettre à disposition et mettre à jour les *assets* (images, CSS, JS).
* Visualiser des informations de *debug*.
* ...

Ces commandes sont disponibles à travers le script php `bin/console` à la racine du projet.

Pour exécuter une commande, il suffit de lancer le script `bin/console` suivi du nom de la commande et de ses arguments.

> ℹ️ À savoir qu'exécuter l'instruction en CLI `php bin/console` ou `php bin/console list` permet d'afficher la liste
> des commandes disponibles (et l'option `--help` disponible pour chaque commande permet d'afficher les informations
> d'aide sur la commande en question).

-----

Au sein du module, nous avons utilisé `Docker` et son plugin `compose` pour monter un environnement de développement. De
cette façon, nous avions notre environnement PHP disponible au sein du service `app`. C'est pourquoi pour exécuter une
commande php, on devait l'exécuter à travers ce service :

```bash
docker compose exec app php bin/console <commande>
# docker: On utilise la commande "docker" qui permet d'interagir avec les images ou les conteneurs Docker.
# compose: On utilise le plugin "compose" qui simplifie la mise en place d'un environnement Docker à travers un fichier
#          de configuration "docker-compose.y(a)ml" ou "compose.y(a)ml".
# exec: Cette commande Docker permet d'exécuter une commande dans un conteneur Docker.
# app: Nom du service, défini dans le fichier de configuration de compose, et qui correspond à notre environnement PHP.
# php bin/console <commande>: Commande à exécuter au sein du conteneur Docker porté par le service "app".
#                             En l'occurrence il s'agit d'exécuter une commande Symfony.
```

## 📜 Commandes utiles

Comme défini précédemment, si vous utilisez l'environnement Docker, vous devrez exécuter toutes les commandes définies
ci-après en préfixant la commande par `docker compose exec app`.

> ⚠️ N'oubliez pas le `docker compose up -d` pour démarrer votre environnement Docker et pouvoir accéder au site ET au
> service "app" pour exécuter vos commandes.

Du coup, pour exécuter la commande `php bin/console list` au sein de l'environnement Docker, il faudra exécuter la
commande `docker compose exec app php bin/console list`.

### 🔨 Commandes génériques

Afficher la liste des commandes Symfony disponibles :

```bash
php bin/console list
```

-----

Vider le cache et le remettre à niveau :

```bash
php bin/console cache:clear
```

### 🗃️ Commandes Doctrine

> ⚠️ Vous devez vous assurer d'avoir bien configuré l'accès à la base de données dans le fichier `.env` de votre projet
> à travers la variable `DATABASE_URL`. Sinon, vous ne pourrez pas vous connecter à la base de données et exécuter les
> commandes de Doctrine.

Créer la base de données (elle est créée automatiquement lors de l'installation du projet, mais si vous l'avez
supprimée, vous pourrez utiliser cette commande pour la recréer) :

```bash
php bin/console doctrine:database:create
```

-----

Créer le schéma de la base de données :

```bash
php bin/console doctrine:schema:create
```

-----

Mettre à jour le schéma de la base de données :

```bash
php bin/console doctrine:schema:update --force
```

-----

Suppression du schéma de la base de données :

```bash
php bin/console doctrine:schema:drop --force
```

-----

Suppression de la base de données :

```bash
php bin/console doctrine:database:drop --force
```

#### 🔃 Migrations

Générer une nouvelle migration à partir des changements du schéma :

```bash
php bin/console make:migration
```

-----

Afficher l'état des migrations :

```bash
php bin/console doctrine:migrations:status
```

-----

Lister les migrations de l'application (exécutées ou pas) :

```bash
php bin/console doctrine:migrations:list
```

-----

Exécuter les migrations latentes :

```bash
php bin/console doctrine:migrations:migrate
```

-----

Exécuter une migration spécifique :

```bash
php bin/console doctrine:migrations:execute --up "DoctrineMigrations\<nom_version>"
```

-----

Annuler une migration spécifique :

```bash
php bin/console doctrine:migrations:execute --down "DoctrineMigrations\<nom_version>"
```

#### 📝 Fixtures

Charger les données *fixtures* dans la base de données :

```bash
php bin/console doctrine:fixtures:load
```

### 💻️ Commandes Maker

Créer une nouvelle entité :

```bash
php bin/console make:entity
```

-----

Créer un CRUD d'entité complet :

```bash
php bin/console make:crud
```

### 🍱️ Assets

Ajouter une dépendance via "importmap" :

```bash
php bin/console importmap:require <package>
```

### 📊️ Debug

Afficher les informations de routage :

```bash
php bin/console debug:router
```

## 📦️ Composer

Le service "app" inclut également Composer, ce qui permet d'exécuter les diverses commandes Composer :

```bash
composer install
composer require <package>
composer remove <package>
```

De la même façon que pour PHP et les commandes Symfony, il faudra préfixer les commandes Composer par
`docker compose exec app` :

```bash
docker compose exec app composer install
```
