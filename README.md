# Affricaffé - PFE

Plateforme web pour café traditionnel tunisien hybride. Réserve, commande en ligne, site vitrine.

## Base de données

**Ce projet n’utilise PostgreSQL pour stocker les données.**  
Toutes les données (panier, comptes utilisateurs, commandes, réservations) sont gérées côté navigateur via l'API backend (PostgreSQL). Pour configurer : 1) Créez la base `affricaffe` dans pgAdmin, 2) Exécutez `server/schema.sql`, 3) `server/.env` avec PGPASSWORD=messai000. Puis `cd server && npm install && npm run dev` pour le backend, et `npm run dev` pour le frontend. Aucune connexion à une base de données n’est requise ni prévue.

## Structure du projet

```
src/
├── components/       # Composants réutilisables
│   ├── Header.jsx
│   ├── Footer.jsx
│   └── ProductCard.jsx
├── context/          # Contexte React (panier)
│   └── CartContext.jsx
├── data/             # Données (produits)
│   └── products.js
├── pages/            # Pages de l'application
│   ├── Home.jsx
│   ├── Menu.jsx
│   ├── Services.jsx
│   ├── Events.jsx
│   ├── Panier.jsx
│   ├── Paiement.jsx
│   ├── Login.jsx
│   └── Register.jsx
├── App.jsx
└── main.jsx
```

## Pages

- **Accueil** – Présentation et réservation
- **Menu** – Catalogue des produits (cafés, boissons, pâtisseries)
- **Services** – Nos services
- **Événements** – Calendrier des événements
- **Panier** – Gestion du panier
- **Paiement** – Finalisation de commande
- **Connexion / Inscription** – Authentification

## Commandes

```bash
npm run dev      # Lancer le serveur de développement
npm run build    # Compiler pour la production
npm run preview  # Prévisualiser le build
```
