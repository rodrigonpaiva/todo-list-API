# To-Do List API

Ceci est le dépôt d'une API pour la création et la gestion d'une liste de tâches (To-Do List) développée en Node.js. L'API permet de créer, lire, mettre à jour et supprimer des tâches, offrant une interface RESTful pour gérer ces opérations.

## Technologies Utilisées

- **Node.js** : Plateforme utilisée pour développer l'API.
- **Express** : Framework pour construire l'API RESTful.
- **Sequelize** : ORM (Object-Relational Mapper) pour interagir avec la base de données PostgreSQL.
- **PostgreSQL** : Base de données utilisée pour stocker les tâches.
- **dotenv** : Gestion des variables d'environnement.
- **validator** : Bibliothèque pour la validation des données.
- **CORS** : Middleware pour permettre le partage de ressources entre différents domaines.

## Installation

### Prérequis

- Node.js (v14.x ou supérieur)
- PostgreSQL

### Étapes d'Installation

1. **Cloner le dépôt :**

   ```bash
   git clone https://github.com/votre-utilisateur/todo-list-api.git
   cd todo-list-api
   ```

2. **Installer les dépendances :**

   Utilisez npm ou yarn pour installer les dépendances du projet.

   ```bash
   npm install
   ```

3. **Configuration de la Base de Données :**

   Créez une base de données PostgreSQL et configurez vos identifiants dans le fichier `.env`. Un exemple de configuration est fourni dans le fichier `.env.example`.

   ```env
   DB_HOST=localhost
   DB_USER=votre_utilisateur
   DB_PASSWORD=votre_mot_de_passe
   DB_NAME=todo_list_db
   DB_PORT=5432
   ```

4. **Exécuter les migrations :**

   Pour configurer les tables de la base de données, exécutez les migrations :

   ```bash
   npx sequelize db:migrate
   ```

5. **Démarrer le serveur :**

   Démarrez le serveur de développement :

   ```bash
   npm run start-dev
   ```

   Le serveur sera disponible à `http://localhost:4000`.

## Endpoints

L'API possède les endpoints suivants :

- **GET /todos** : Retourne toutes les tâches.
- **GET /todos/:id** : Retourne une tâche spécifique par son ID.
- **POST /todos** : Crée une nouvelle tâche.
- **PUT /todos/:id** : Met à jour une tâche existante par son ID.
- **DELETE /todos/:id** : Supprime une tâche par son ID.

### Exemple de Requête - Créer une Tâche

```http
POST /todos
Content-Type: application/json

{
  "id": 1,
  "title": "Acheter du pain",
  "done": false
}
```

### Exemple de Requête - Lister les Tâches

```http
GET /todos
```

## Variables d'Environnement

Les variables d'environnement suivantes sont utilisées dans le projet :

- `DB_HOST` : Hôte de la base de données.
- `DB_USER` : Utilisateur de la base de données.
- `DB_PASSWORD` : Mot de passe de la base de données.
- `DB_NAME` : Nom de la base de données.
- `DB_PORT` : Port de connexion à la base de données.

## Scripts

- `npm run start-dev` : Démarre le serveur en mode développement avec nodemon.

## Dépendances

- **cors** : ^2.8.5
- **dotenv** : ^10.0.0
- **express** : ^4.17.1
- **pg** : ^8.7.1
- **pg-hstore** : ^2.3.4
- **sequelize** : ^6.6.5
- **validator** : ^13.6.0

## Dépendances de Développement

- **@types/cors** : ^2.8.12
- **@types/express** : ^4.17.13
- **@types/node** : ^16.6.1
- **@types/sequelize** : ^4.28.10
- **@types/validator** : ^13.6.3

## Licence

Ce projet est sous licence [MIT License](./LICENSE).

---

Fait avec 💻 par [Rodrigo Paiva](https://github.com/rodrigonpaiva).
