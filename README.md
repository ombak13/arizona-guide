# Grand Circle — Arizona & Utah 🏜️

Guide de voyage interactif pour un road trip solo Arizona/Utah — 12 nuits, 4→16 novembre 2026.
Application web autonome (HTML/CSS/JS, zéro dépendance, zéro build), installable comme app sur mobile et utilisable **hors-ligne**.

## Contenu

- **Programme** — jour par jour ou par catégorie, avec hébergements, distances et points forts
- **Carte** — tracé Phoenix → Vegas dessiné (relief, fleuve Colorado, déserts), 18 étapes cliquables vers Google Maps
- **Checklist** — réservations + équipement, cochage sauvegardé automatiquement
- **Budget** — estimatif par poste + saisie du dépensé réel, sauvegardé automatiquement

## Fichiers

```
arizona-guide/
├── index.html        ← le guide (tout est dedans)
├── manifest.json     ← config app installable (PWA)
├── sw.js             ← service worker (cache hors-ligne)
├── icon-192.png      ← icônes app
├── icon-512.png
├── icon-180.png      ← icône iOS (apple-touch-icon)
├── .nojekyll         ← désactive Jekyll sur GitHub Pages
└── README.md
```

## Déploiement sur GitHub Pages

1. Créer un dépôt GitHub (ex. `arizona-guide`).
2. Y déposer **tous les fichiers ci-dessus** à la racine du dépôt.
3. Dans le dépôt : **Settings → Pages**.
4. Sous *Build and deployment*, choisir **Deploy from a branch**, branche `main`, dossier `/ (root)`, puis **Save**.
5. Attendre 1-2 min. Le guide est en ligne à :
   `https://<ton-pseudo>.github.io/arizona-guide/`

## Installer comme app sur iPhone

1. Ouvrir l'URL ci-dessus dans **Safari**.
2. Bouton Partager → **Sur l'écran d'accueil**.
3. L'icône mesa apparaît comme une vraie app. Au premier chargement avec réseau, le guide se met en cache : il restera consultable **hors-ligne** (utile dans les zones désertiques sans signal).

## Notes

- Les données de la checklist et du budget sont stockées **localement sur l'appareil** (localStorage). Elles ne se synchronisent pas entre iPhone et ordinateur.
- Pour mettre à jour le cache hors-ligne après une modification, augmenter la version dans `sw.js` (`arizona-guide-v1` → `v2`).
