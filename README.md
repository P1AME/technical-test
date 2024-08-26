# Test Technique - Développement d'une Application Web avec Symfony & React

## Objectif

Ce test a pour objectif d'évaluer vos compétences dans la mise en place d'une application complète utilisant Symfony pour le backend et React pour le frontend, le tout orchestré avec Docker. Vous devrez également gérer les données via une base de données PostgreSQL accessible via PgAdmin.

## Prérequis

Avant de commencer, assurez-vous d'avoir les outils suivants installés :

- **Git**
- **Docker** et **Docker Compose**
- Un éditeur de code (VS Code, PHPStorm, etc.)

## Instructions

### Communication du résultat

- Des commits réguliers devront être poussés afin de comprendre l'ordre dans lequel le projet a été réalisé.
- Les commits devront êtré nommés de façon à pouvoir identifier la fonctionnalité mise en place / mise à jour.
- Pour démarrer le projet vous devrez cloner le dépot GIT.
- Vous créérez votre dépôt vers lequel vous pousserez le résultat et vous m'ajouterez (P1AME) en tant que Viewer.

### Structure du Projet

##### Description

Ce projet consiste à développer une application web complète en utilisant Symfony pour le backend et React pour le frontend, le tout orchestré via Docker. L'application permet la gestion de produits, de catégories et de paniers d'achat à travers une interface utilisateur stylisée et des API RESTful. Le backend est responsable de la gestion des données et des opérations CRUD (Create, Read, Update, Delete) sur les entités produits, catégories, et paniers, tandis que le frontend fournit des interfaces utilisateur pour interagir avec ces données.

##### Fonctionnalités Clés :

- CRUD Produits : Gestion des produits avec des attributs tels que nom, catégorie, référence, image, prix, quantité en stock, etc.
- CRUD Catégories : Gestion des catégories de produits.
- CRUD Paniers : Gestion des paniers, y compris l'ajout de produits, calcul du prix total, et suivi du statut de paiement.

#### Backend Symfony

- Créez un projet Symfony dans le répertoire `backend/`.
- Configurez une base de données PostgreSQL accessible via Docker.
- Configurez Docker pour lancer l'environnement Symfony, PostgreSQL, et PgAdmin.

#### Frontend React

- Créez un projet React dans le répertoire `frontend/`.
- Configurez Docker pour lancer l'application React.
- Utilisez un template existant pour styliser l'interface ou créez votre propre design.

#### Base de Données (PostgreSQL + PgAdmin)

- Configurez une base de données PostgreSQL pour gérer les entités.
- Assurez-vous que PgAdmin est accessible pour la gestion de la base de données via l'interface graphique.

### Backend (Symfony)

#### Entité Produit

- **Attributs** : `id`, `nom`, `categorie`, `référence`, `image`, `prix unitaire`, `quantité en stock`, `date de création`, `date de modification`.
- Implémentez le CRUD complet pour l'entité `Produit` via des routes API.

#### Entité Catégorie

- **Attributs** : `id`, `nom`, `date de création`, `date de modification`.
- Implémentez le CRUD complet pour l'entité `Catégorie` via des routes API.

#### Entité Panier

- **Attributs** : `id`, `produits dans le panier`, `utilisateur (facultatif)`, `prix total`, `is paid`.
- Implémentez le CRUD complet pour l'entité `Panier` via des routes API.

### Frontend (React)

#### Interfaces Utilisateur

- Créez des interfaces stylisées permettant le CRUD pour les entités `Produit`, `Catégorie`, et `Panier`.
- Vous pouvez utiliser un template existant pour le design des interfaces.

### Fonctionnalités **Facultatives**

#### Authentification Utilisateur

- Implémentez un système d'authentification simple avec gestion des mots de passe.
- Protégez les routes API et l'accès au backend via un mécanisme de sécurité (JWT, session, etc.).

#### Gestion du Panier

- Ajoutez la fonctionnalité permettant de rendre un panier "payé".
- Implémentez une séparation des environnements front-office et back-office (espace client et espace administrateur).

#### Génération de Facture

- Implémentez la génération de factures pour les paniers payés.

#### Envoi de Mail de Confirmation

- Configurez un service d'envoi d'emails pour envoyer une confirmation de commande.
- Utilisez un SMTP fictif via Docker pour simuler l'envoi de mails.

### Docker Configuration

#### Fichier `docker-compose.yml`

- Créez un fichier `docker-compose.yml` à la racine du projet avec les services suivants :
  - **backend** : Conteneur pour le backend Symfony.
  - **frontend** : Conteneur pour le frontend React.
  - **database** : Conteneur PostgreSQL pour la base de données.
  - **pgadmin** : Conteneur pour PgAdmin pour la gestion de la base de données.
  - **smtp** (facultatif) : Conteneur pour un serveur SMTP fictif si vous implémentez l'envoi de mails.

#### Volumes & Réseaux

- Assurez-vous que les volumes sont correctement configurés pour la persistance des données.
- Configurez un réseau Docker pour permettre la communication entre les services.

## Critères d'Évaluation

- **Fonctionnalité** : Le module fonctionne-t-il comme attendu ?
- **Qualité du Code** : Le code est-il bien structuré et lisible ?
- **Respect des Consignes** : Avez-vous respecté les spécifications fournies ?
- **Dockerisation** : Le projet est-il correctement dockerisé et facile à démarrer ?
- **Implémentation des Fonctionnalités Facultatives** : Si vous avez choisi d'implémenter des fonctionnalités avancées, elles seront prises en compte dans l'évaluation.

## Livrables

### Code Source

- Le code source doit être organisé et documenté.
- Les migrations et seeders de base de données doivent être inclus pour initialiser les données de base.

### Documentation

- Fournissez un fichier `README.md` avec des instructions claires sur la mise en place du projet, y compris la configuration Docker, l'installation, et les commandes de base pour démarrer les services.
- Si vous avez implémenté des fonctionnalités avancées, expliquez vos choix et comment les tester.

### Conclusion
Merci d'avoir participé à ce test technique. Votre soumission sera évaluée en fonction des critères mentionnés ci-dessus. Si vous avez des questions ou des problèmes, n'hésitez pas à les mentionner dans votre documentation.

## Bon courage !
