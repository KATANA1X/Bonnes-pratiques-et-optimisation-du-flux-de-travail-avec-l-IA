# Checkpoint : Réparation et Refactorisation d'un Composant Carte de Prix

## 🤖 Prompt IA utilisée

> *"Identifie et corrige les erreurs HTML et CSS dans ce composant de carte de prix (faute de frappe sur box-shadow, balise h2 mal fermée et ergonomie du bouton). Refactorise ensuite le code en une fonction JavaScript réutilisable `Card(title, price, features, buttonText, isPopular, index)` qui génère dynamiquement plusieurs cartes dans le DOM avec des animations modernes (apparition en cascade, survol dynamique, effet d'onde au clic et notification toast)."*

---

## 🐛 Résumé des bogues identifiés et corrigés

### 1. Syntaxe et mise en page (HTML / CSS)
* **Faute de frappe CSS (`box-shdow`) :** Correction en `box-shadow` avec une ombre portée moderne et douce.
* **Balise HTML non fermée (`<h2>`) :** Correction de `<h2 class="title">Basic Plan<h2>` en `<h2 class="title">Basic Plan</h2>` pour rétablir la validité sémantique du DOM.
* **Disposition et design :** Remplacement du bloc statique par une mise en page flexible (`display: flex`) responsive avec carte mise en avant (`badge` "Populaire") et animations fluides (`@keyframes fadeInUp`).

### 2. Interactivité et expérience utilisateur (UX)
* **Curseur et retour visuel :** Ajout de `cursor: pointer`, d'effets de surélévation au survol (`translateY`) et d'une animation d'onde circulaire (`ripple`) au clic sur le bouton.
* **Notification dynamique :** Remplacement de l'absence d'action par un système de notification **Toast** moderne confirmant l'offre sélectionnée.

### 3. Refactorisation en composant réutilisable
* **Génération dynamique :** Création de la fonction `Card()` permettant d'instancier autant de cartes que nécessaire à partir d'un tableau de données.

---