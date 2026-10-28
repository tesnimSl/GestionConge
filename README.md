# Suivi des congés

Application web (HTML/CSS/JS, sans dépendance ni build) de suivi des congés payés et maladie : tableau de bord, suivi mensuel, calendrier, prévisions réel/prévisionnel, opérations CRUD, historique, corrections de solde, export CSV, sauvegarde JSON, tests de calcul intégrés (Paramètres → « Lancer les tests de calcul »). Installable (PWA) et utilisable hors ligne.

## Déploiement sur GitHub Pages
1. Créez un dépôt GitHub et poussez ces fichiers à la racine (`git init && git add . && git commit -m "init" && git branch -M main && git remote add origin <url> && git push -u origin main`).
2. Dépôt → Settings → Pages → Source : « Deploy from a branch », branche `main`, dossier `/ (root)`.
3. L’application est disponible sur `https://<utilisateur>.github.io/<dépôt>/` (HTTPS requis pour l’installation).

## Installation
- Android / PC (Chrome, Edge) : menu du navigateur → « Installer l’application ».
- iOS (Safari) : Partager → « Sur l’écran d’accueil ».

## Limites importantes
- Données stockées dans le navigateur de chaque appareil (localStorage) : pas de synchronisation entre appareils ni de comptes. Utilisez Paramètres → Sauvegarder / Restaurer pour transférer.
- GitHub Pages est statique : une vraie authentification multi-utilisateurs exige un backend (ex. Supabase ou Firebase) à brancher à la place de `save()` / `load()` dans `index.html`.
- Exports Excel (.xlsx) et PDF non implémentés (CSV et impression navigateur disponibles).
