# 724 Events - Correction et Optimisation de la Plateforme Événementielle

Ce projet consiste en la finalisation, le débogage et l'assurance qualité du site vitrine de l'agence événementielle **724 Events**.

L'application est construite avec **React** et utilise une suite de tests automatisés (**Jest** / **React Testing Library**) ainsi qu'une approche **BDD (Behavior-Driven Development)** pour valider les parcours utilisateurs.

<img width="600" alt="screenshot-724-events" src="https://github.com/user-attachments/assets/44868d42-5fd3-46c9-92da-748e9ab769fa" />


---

## 🛠️ Stack Technique

* **Front-end :** React 18, JSX, SCSS / CSS Modules
* **Tests :** Jest, React Testing Library
* **Méthodologie de recette :** BDD (Behavior-Driven Development)
* **Gestionnaire de paquets :** Yarn

---

## 🚀 Correctifs Appliqués

Au cours du projet, l'intégralité des anomalies identifiées a été résorbée :

1. **Helper `Date` (`src/helpers/Date/index.js`) :**
   * Correction de la fonction `getMonth` pour supprimer le décalage d'un mois dû à l'indexation de l'objet `Date` en JavaScript (`0` pour janvier).

2. **Contexte de données (`src/contexts/DataContext/index.js`) :**
   * Ajout de la logique de calcul de l'événement le plus récent (`last`).
   * Injection de la propriété `last` dans la valeur du `DataContext.Provider`.
   * Optimisation des appels asynchrones avec `useCallback` et gestion propre du cycle de vie avec `useEffect`.

3. **Composant `Select` (`src/components/Select/index.js`) :**
   * Transmission effective du paramètre `newValue` lors de l'appel à la fonction `onChange`.

4. **Composant `EventList` (`src/containers/Events/index.js`) :**
   * Mise en place du filtrage par catégorie (`eventsByType`) couplé à la pagination par tranche de 9 éléments.

5. **Carrousel `Slider` (`src/containers/Slider/index.js`) :**
   * Tri immuable des événements phares par date décroissante.
   * Correction de la gestion des index et des clés d'affichage.

6. **Navigation & Accessibilité (`src/pages/Home/index.js`) :**
   * Ajout des attributs `id` manquants (`nos-services`, `nos-realisations`, `notre-equipe`, `contact`) pour activer les liens d'ancrage du menu.
   * Fixation du menu en haut de page (`position: fixed`) pour améliorer l'expérience utilisateur.

---

## 🧪 Tests Automatisés

Toutes les suites de tests unitaires et d'intégration sont au vert (100% de réussite).

Pour lancer les tests automatisés :

```bash
# Exécution de la suite de tests
yarn test

# Exécution avec détails verbeux
yarn test --verbose --watchAll=false
````

## 📄 Cahier de Recette (BDD)

Un cahier de recette fonctionnel rédigé en syntaxe **Gherkin** (_Étant donné que / Quand / Alors_) est disponible dans la documentation du projet. Il détaille l'ensemble des scénarios de test end-to-end couvrant :

- Le défilement et l'affichage du carrousel.

- Le filtrage dynamique des réalisations.
 
- La soumission du formulaire de contact et l'ouverture de la modale de confirmation.

- L'affichage de la dernière prestation dans le pied de page.


## 💻 Installation et Lancement du Projet

### Prérequis

- **Node.js** (version 16+ recommandée)
- **Yarn**

### Étapes d'installation

1. **Cloner le dépôt :**

```bash
git clone https://github.com/Sereta80/OC-P9_Debuggez-une-application-React.JS.git
cd OC-P9_Debuggez-une-application-React
```

   
2. **Installer les dépendances :**
```
yarn install
```

3. **Lancer le serveur de développement :**
```bash
yarn start
```

L'application sera accessible à l'adresse `http://localhost:3000`.

---

*Séréta THAI - Étudiante Intégratrice Web chez OpenClassrooms 2026*
