# Guide de Contribution

## Structure des Branches

Nous utilisons un modèle de branches basé sur les fonctionnalités :

- `main` : Code stable et déployable
- `develop` : Branche d'intégration pour les nouvelles fonctionnalités
- `feature/[nom-fonctionnalité]` : Branches pour développer de nouvelles fonctionnalités
- `fix/[nom-bug]` : Branches pour corriger des bugs

## Workflow de Développement

1. Créer une branche à partir de `develop` pour votre fonctionnalité ou correctif
2. Implémenter les changements
3. Soumettre une Pull Request vers `develop`
4. Après revue et validation, la PR est fusionnée dans `develop`
5. Périodiquement, `develop` est fusionné dans `main` pour les releases

## Standards de Code

### Général

- Utiliser des noms explicites pour les variables, fonctions et composants
- Commenter le code pour les parties complexes
- Écrire des tests unitaires pour les fonctionnalités critiques

### React

- Utiliser des fonctions composants avec hooks
- Séparer la logique métier et la présentation
- Réutiliser les composants autant que possible
- Optimiser les rendus avec useMemo, useCallback, etc.

### TypeScript

- Définir des interfaces pour tous les props de composants
- Utiliser des types précis plutôt que `any`
- Documenter les interfaces complexes

### CSS / Styling

- Suivre la charte graphique définie
- Utiliser des variables CSS pour les couleurs et dimensions
- Assurer la responsivité sur tous les composants

## Pull Requests

Chaque PR doit inclure :

1. Description des changements
2. Référence aux issues concernées
3. Screenshots ou captures pour les changements visuels
4. Liste des tests effectués

## Revue de Code

Lors de la revue, vérifier :

1. La qualité et la lisibilité du code
2. Le respect des standards de développement
3. La performance et l'optimisation
4. La couverture de test adéquate
5. La compatibilité avec les différents navigateurs

## Conventions de Commit

Nous utilisons des messages de commit conventionnels :

- `feat:` Nouvelle fonctionnalité
- `fix:` Correction de bug
- `docs:` Changements dans la documentation
- `style:` Formatage, point-virgules manquants, etc.
- `refactor:` Refactorisation du code
- `test:` Ajout ou correction de tests
- `chore:` Modifications diverses non relatives au code source

Exemple : `feat: ajouter la carte interactive des fournisseurs`