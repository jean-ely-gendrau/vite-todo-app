# TodoList React

Application de gestion de taches construite avec React et Vite.

## Fonctionnalites

- Ajouter des taches avec validation
- Marquer les taches comme terminees
- Modifier le texte des taches
- Supprimer des taches individuellement
- Filtrer par statut (Toutes / Actives / Terminees)
- Statistiques en temps reel
- Persistance des donnees (localStorage)
- Bouton pour tout supprimer

## Technologies

- React 19
- Vite 7
- Tailwind CSS 4

## Installation

```bash
npm install
```

## Developpement

```bash
npm run dev
```

L'application sera disponible sur `http://localhost:5173`

## Build

```bash
npm run build
```

## Structure du projet

```
src/
├── components/
│   ├── TodoForm.jsx      # Formulaire d'ajout
│   ├── TodoItem.jsx      # Element de tache
│   ├── TodoList.jsx      # Liste des taches
│   ├── TodoFilter.jsx    # Boutons de filtre
│   └── TodoStats.jsx     # Statistiques
├── hooks/
│   ├── useLocalStorage.js  # Hook de persistance
│   └── useTodos.js         # Hook de gestion CRUD
├── App.jsx
├── App.css
└── main.jsx
```

## Hooks personnalises

### useLocalStorage

Synchronise un state React avec le localStorage du navigateur.

```jsx
const [value, setValue] = useLocalStorage('key', initialValue);
```

### useTodos

Gere les operations CRUD sur les taches.

```jsx
const { todos, ajouterTodo, toggleTodo, supprimerTodo, editerTodo, toutSupprimer } = useTodos();
```

## Evolutions prevues

- Authentification utilisateur
- Backend API avec MySQL
- Categories de taches
- Dates limites
