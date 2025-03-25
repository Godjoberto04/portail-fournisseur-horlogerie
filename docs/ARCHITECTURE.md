# Architecture du Projet

## Vue d'Ensemble

Le portail fournisseur est structuré comme une application React moderne avec TypeScript, en suivant une architecture modulaire et évolutive.

## Structure des Dossiers

```
src/
├── components/           # Composants réutilisables
│   ├── common/           # Éléments UI de base (boutons, inputs, etc.)
│   ├── dashboard/        # Composants spécifiques au dashboard
│   ├── forms/            # Composants de formulaire
│   ├── layout/           # Composants structurels (header, sidebar, etc.)
│   ├── maps/             # Composants pour la carte interactive
│   ├── charts/           # Visualisations et graphiques
│   └── tables/           # Tableaux et grilles de données
├── pages/                # Pages principales de l'application
├── layouts/              # Templates de mise en page
├── hooks/                # Custom hooks React
├── context/              # Context providers
├── services/             # Services d'API et utilitaires
│   ├── api/              # Service de requêtes API (simulées)
│   └── auth/             # Service d'authentification
├── styles/               # Styles globaux et thèmes
├── utils/                # Fonctions utilitaires
├── types/                # Définitions TypeScript
├── data/                 # Données de démonstration
└── App.tsx               # Point d'entrée de l'application
```

## Principes Architecturaux

### Séparation des Préoccupations

Chaque composant a une responsabilité unique et bien définie. Les composants de présentation sont séparés de la logique métier.

### Modularité

Les composants sont conçus pour être modulaires et réutilisables. Ils acceptent des props bien définies pour personnaliser leur comportement.

### État Global

L'état global de l'application est géré via React Context pour simplifier la communication entre composants distants et éviter le "prop drilling".

### Gestion des Données

Les données sont chargées et mises en cache à partir de services simulés d'API. Cela facilitera l'intégration future avec une API réelle.

## Patterns Utilisés

### Compound Components

Utilisé pour les composants complexes avec plusieurs sous-composants qui partagent un état interne.

### Render Props / Higher-Order Components

Utilisés pour partager la logique entre composants lorsque nécessaire.

### Custom Hooks

Extraction de la logique réutilisable dans des hooks personnalisés pour simplifier les composants.

## Flux de Données

1. Les services récupèrent les données (simulées localement)
2. Les données sont stockées dans les contexts appropriés
3. Les composants consomment ces données via hooks personnalisés
4. Les actions utilisateur déclenchent des mises à jour via les fonctions exposées par les contexts

## Performance

- Utilisation de `React.memo` pour empêcher les rendus inutiles
- Memoization des calculs coûteux avec `useMemo`
- Stabilisation des références de fonction avec `useCallback`
- Utilisation de la lazy loading pour les composants volumineux

## Sécurité

Bien que ce soit un prototype, nous simulons les bonnes pratiques de sécurité :

- Authentification par JWT (simulée)
- Contrôle d'accès basé sur les rôles
- Validation des entrées utilisateur
- Protection contre les attaques XSS