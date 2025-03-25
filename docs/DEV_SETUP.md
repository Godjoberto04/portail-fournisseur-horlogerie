# Guide d'installation et de développement

## Prérequis

- Node.js (version 20.x ou supérieure recommandée)
- npm (version 10.x ou supérieure) ou yarn (version 1.22.x ou supérieure)
- Git

## Installation

1. Cloner le dépôt GitHub

```bash
git clone https://github.com/Godjoberto04/portail-fournisseur-horlogerie.git
cd portail-fournisseur-horlogerie
```

2. Installer les dépendances

```bash
# Avec npm
npm install

# Ou avec yarn
yarn install
```

3. Lancer le serveur de développement

```bash
# Avec npm
npm run dev

# Ou avec yarn
yarn dev
```

L'application sera accessible à l'adresse [http://localhost:3000](http://localhost:3000).

## Structure du projet

```
/
├── docs/               # Documentation du projet
├── design/             # Maquettes et assets graphiques
├── public/             # Fichiers statiques
├── src/                # Code source
│   ├── assets/         # Images, icônes, etc.
│   ├── components/     # Composants React réutilisables
│   ├── context/        # Context API pour la gestion d'état
│   ├── data/           # Données de démonstration
│   ├── hooks/          # Custom hooks
│   ├── layouts/        # Layouts de l'application
│   ├── pages/          # Pages de l'application
│   ├── services/       # Services (API, auth, etc.)
│   ├── styles/         # Styles globaux et thèmes
│   ├── types/          # Types TypeScript
│   ├── utils/          # Fonctions utilitaires
│   ├── App.tsx         # Composant racine
│   └── main.tsx        # Point d'entrée
├── .eslintrc.js        # Configuration ESLint
├── .prettierrc         # Configuration Prettier
├── tsconfig.json       # Configuration TypeScript
├── vite.config.ts      # Configuration Vite
└── package.json       # Dépendances et scripts
```

## Conventions de développement

### Composants

- Chaque composant doit être dans son propre dossier avec la structure suivante :

```
ComponentName/
├── index.ts              # Export du composant
├── ComponentName.tsx     # Code du composant
├── ComponentName.styles.ts # Styles du composant (si applicable)
├── ComponentName.types.ts # Types du composant
└── ComponentName.test.tsx # Tests unitaires
```

### Imports

- Organiser les imports dans l'ordre suivant :
  1. Imports de bibliothèques externes
  2. Imports de composants
  3. Imports de hooks
  4. Imports de contextes
  5. Imports de services
  6. Imports d'utilitaires
  7. Imports de types
  8. Imports de styles

### Nommage

- **Composants** : PascalCase (ex: `DashboardCard`)
- **Fonctions** : camelCase (ex: `formatDate`)
- **Variables** : camelCase (ex: `userData`)
- **Types/Interfaces** : PascalCase avec préfixe I pour les interfaces (ex: `IUserData`)
- **Fichiers de composants** : PascalCase (ex: `DashboardCard.tsx`)
- **Autres fichiers** : camelCase (ex: `authService.ts`)

## Scripts disponibles

- `npm run dev` : Lance le serveur de développement
- `npm run build` : Compile l'application pour la production
- `npm run preview` : Prévisualise la version de production
- `npm run lint` : Vérifie le code avec ESLint
- `npm run lint:fix` : Corrige automatiquement les problèmes d'ESLint
- `npm run format` : Formate le code avec Prettier
- `npm run test` : Lance les tests unitaires

## Workflow Git

1. Créer une nouvelle branche à partir de `develop` pour chaque fonctionnalité ou correctif

```bash
git checkout develop
git pull
git checkout -b feature/nom-de-la-fonctionnalite
```

2. Faire des commits réguliers avec des messages clairs

```bash
git add .
git commit -m "feat: description de la fonctionnalité"
```

3. Pousser la branche vers le dépôt distant

```bash
git push -u origin feature/nom-de-la-fonctionnalite
```

4. Créer une Pull Request vers la branche `develop`

5. Après revue et validation, fusionner la PR dans `develop`

## Ressources

- [Documentation React](https://reactjs.org/docs/getting-started.html)
- [Documentation TypeScript](https://www.typescriptlang.org/docs/)
- [Documentation Styled Components](https://styled-components.com/docs)
- [Documentation React Router](https://reactrouter.com/en/main)