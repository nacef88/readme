# readme
Projet développement Web
# PADDel

## Description
PADDel est une application de gestion de club de padel, conçue pour faciliter l'administration des terrains, la réservation, la publication d'articles de blog, la gestion d'une boutique et le suivi des utilisateurs.

### Objectif
- Automatiser la gestion des infrastructures (terrains, réservations).
- Offrir une plateforme de communication via un blog.
- Gérer un store en ligne pour les équipements.
- Assurer un système sécurisé d'inscription et de gestion des utilisateurs.

## Table des matières
1. [Installation](#installation)
2. [Configuration](#configuration)
3. [Utilisation](#utilisation)
4. [Structure du projet](#structure-du-projet)
5. [Contribution](#contribution)
6. [Licence](#licence)

## Installation
1. **Cloner le dépôt**
    ```bash
    git clone https://votre-repo.git
    cd paddel
    ```
2. **Installer les dépendances Backend**
    ```bash
    cd backend
    npm install    # ou composer install / mvn install selon le stack
    ```
3. **Installer les dépendances Frontend**
    ```bash
    cd ../frontend
    npm install
    ```

## Configuration
1. Copier le fichier d'exemple d'environnement :
    ```bash
    cp .env.example .env
    ```
2. Modifier les variables dans `.env` :
    - `DB_HOST`, `DB_USER`, `DB_PASS`, `DB_NAME`
    - Clés SMTP pour l'envoi d'emails
    - Clés API externes (paiement, cartographie…)

## Utilisation
1. **Démarrer le Backend**
    ```bash
    cd backend
    npm run start    # ou php bin/console server:run / mvn spring-boot:run
    ```
2. **Démarrer le Frontend**
    ```bash
    cd ../frontend
    npm run dev
    ```
3. Ouvrir votre navigateur à l'adresse : `http://localhost:3000`

## Structure du projet
- **backend/** : API, logique métier, gestion de la BDD
- **frontend/** : interface utilisateur (HTML6, CSS3, JavaScript)
- **docs/** : documentation et guides
- **.github/** : workflows CI/CD (GitHub Actions)

### Modules
| Module                   | Fonctionnalités principales                                           |
|--------------------------|------------------------------------------------------------------------|
| Gestion de Terrains      | Création, modification, suppression, calendrier de disponibilités      |
| Gestion de Réservation   | Réservations, annulations, modifications, notifications par email      |
| Blog                     | Publication d'articles, catégories, tags, commentaires, modération     |
| Gestion de Stores        | Catalogue produits, gestion de stock, commandes, paiement en ligne     |
| Users                    | Inscription, authentification (JWT/OAuth), profils, permissions         |

## Contribution
Les contributions sont les bienvenues ! 
1. Forkez ce dépôt
2. Créez une branche `feature/ma-fonctionnalite`
3. Committez vos changements : `git commit -m "Ajout de ma fonctionnalité"`
4. Pushez votre branche : `git push origin feature/ma-fonctionnalite`
5. Ouvrez une Pull Request

Merci de respecter les bonnes pratiques de code et d'ajouter des tests si nécessaire.

## Licence
Ce projet est sous licence MIT. Consultez le fichier [LICENSE](./LICENSE) pour plus de détails.
