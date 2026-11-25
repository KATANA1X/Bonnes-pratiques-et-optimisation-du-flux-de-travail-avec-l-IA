<!-- Section 1 : Prompt IA utilisée dans Cursor -->
## 🤖 Prompt IA utilisée

> *"Identifie et corrige les erreurs HTML et CSS dans ce composant de carte de prix (comme la faute de frappe sur box-shadow, la balise h2 mal fermée et le style du bouton). Ensuite, refactorise ce code pour créer une fonction JavaScript réutilisable `Card(title, price, features, buttonText)` qui génère dynamiquement plusieurs cartes dans le DOM et ajoute une interaction au clic sur le bouton."*

---

<!-- Section 2 : Liste des bogues corrigés -->
## 🐛 Résumé des bogues identifiés et corrigés

### 1. Problèmes de mise en page et de syntaxe (HTML / CSS)
* **Faute de frappe CSS (`box-shdow`) :** Correction de `box-shdow: 0 0 10px #ccc;` en `box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);` pour restaurer l'ombre portée de la carte.
* **Balise HTML non fermée (`<h2>`) :** Correction de `<h2 class="title">Basic Plan<h2>` en `<h2 class="title">Basic Plan</h2>` (ajout du `/` manquant) afin de garantir la validité sémantique du DOM.
* **Alignement et espacement :** Ajout d'un conteneur flexible (`display: flex` et `gap: 20px`) pour permettre l'affichage harmonieux de plusieurs cartes côte à côte sur différentes tailles d'écran.

### 2. Problèmes d'interactivité et d'ergonomie
* **Curseur du bouton :** Ajout de `cursor: pointer;` sur la classe `.btn` pour indiquer visuellement que le bouton est cliquable au survol.
* **Action au clic manquante :** Ajout d'un écouteur d'événement JavaScript (`addEventListener('click', ...)`) sur chaque bouton afin qu'il déclenche une réaction dynamique lors du clic.

### 3. Refactorisation en composant réutilisable
* **Suppression du code en dur :** Remplacement de la carte statique HTML par une fonction JavaScript `Card(title, price, features, buttonText)` qui génère et injecte dynamiquement les cartes dans le DOM à partir d'un tableau de données.

