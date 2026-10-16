# Devenir tech lead en 8 semaines — PWA

Application installable sur téléphone et ordinateur, utilisable hors ligne.

## Contenu

- `index.html` : la page (identique à l'artefact, avec le manifeste, le service worker et un bandeau d'installation)
- `manifest.webmanifest` : nom, couleurs, icônes
- `sw.js` : service worker (cache de la page, des icônes et des polices)
- `icons/` : icônes 192, 512, maskable, Apple et favicon

## Mettre en ligne

Une PWA doit être servie en **HTTPS**. Trois options gratuites :

1. **Netlify Drop** : glissez le dossier sur https://app.netlify.com/drop
2. **GitHub Pages** : poussez le dossier dans un dépôt, puis Settings → Pages → branche `main`, dossier racine
3. **Cloudflare Pages** ou **Vercel** : importez le dossier, aucune configuration nécessaire

Pour tester en local : `python3 -m http.server 8000` puis http://localhost:8000 (localhost est accepté sans HTTPS).

## Installer

- **Android / Chrome / Edge** : un bandeau « Installer » apparaît en haut de la page.
- **iPhone / iPad** : Safari → Partager → « Sur l'écran d'accueil ».

## Publier une modification

Après avoir modifié `index.html`, changez `VERSION` en tête de `sw.js` (par ex. `"v2"`).
L'application proposera « Mettre à jour » à la prochaine ouverture.

## Progression

Hors de claude.ai, les cases cochées sont enregistrées dans le navigateur de l'appareil
(pas de synchronisation entre appareils). Effacer les données du site efface la progression.
