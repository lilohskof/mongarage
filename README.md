# MonGarage

Journal d'entretien auto et moto, PWA hors-ligne, **variante locale** du cahier des charges (sans compte ni serveur). Les donnees restent dans IndexedDB sur l'appareil.

## Contenu V1 locale
- Vehicules (voiture, moto, scooter, utilitaire), archivage, suppression avec confirmation
- Journal d'entretien (date, km, categorie, cout facultatif, garage, notes), filtre par categorie
- Releves kilometriques, alerte de kilometrage incoherent, "kilometrage a actualiser"
- Rappels par date et/ou km, recalcul propose apres validation, statut en texte (pas seulement en couleur)
- Depenses par categorie et periode, estimation du cout au km
- Export JSON / CSV, import JSON (fusion), vue imprimable pour PDF
- Hors-ligne (service worker), installable

## Pas encore fait
Photos et pieces jointes, comptes et synchronisation (D1), partage, notifications, tests automatises, icones PNG 192/512.

## Deploiement Cloudflare Pages
1. Cloudflare > Workers & Pages > Create > Pages > Connect to Git, choisir ce depot.
2. Framework preset: None. Build command: (vide). Build output directory: `/`.
3. Deployer, puis ouvrir l'URL `*.pages.dev` sur le telephone et choisir "Installer l'application" / "Ajouter a l'ecran d'accueil".

## Test local
`python3 -m http.server 8000` puis http://localhost:8000

## Sauvegarde
Exporter regulierement le JSON (Plus > Reglages). Vider les donnees du navigateur efface le carnet.
