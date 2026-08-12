# Changelog

Toutes les modifications notables de ce projet sont documentées dans ce fichier.

Le format suit [Keep a Changelog](https://keepachangelog.com/fr/1.0.0/) et ce projet suit le [Semantic Versioning](https://semver.org/lang/fr/).

## [1.3.2] - 2026-08-12

### Corrigé
- Le statut "lu" (article grisé) était perdu au rafraîchissement à cause de paramètres de tracking variables dans les URLs des flux RSS. Les liens sont désormais normalisés (domaine + chemin, sans query params) avant comparaison, ce qui rend le marquage persistant et fiable.

## [1.3.1] - 2026-08-12

### Corrigé
- Le dashboard pouvait rester bloqué indéfiniment sur "synchronisation en cours" si un flux RSS ou une requête de stockage ne répondait pas. Ajout d'un timeout de 12s par flux et de 5s par appel de stockage.
- Ajout d'un état d'erreur visible (point rouge + message clair) en cas d'échec de synchronisation, avec nouvelle tentative automatique au prochain refresh.

## [1.3.0] - 2026-08-12

### Ajouté
- Rééquilibrage des sources : chaque catégorie combine désormais un flux anglophone et un flux francophone.
  - IA : MIT Technology Review (EN) + Actu IA (FR)
  - Dev & Web : Hacker News (EN) + Journal du Hacker (FR)
  - Tech Général : TechCrunch (EN) + Numerama (FR)

## [1.2.0] - 2026-01-02

### Ajouté
- Marquage des articles comme lus au clic (grisés, titre barré), avec mémorisation persistante entre les sessions.

## [1.1.0] - 2025-08-30

### Ajouté
- Rafraîchissement automatique des flux toutes les heures, avec compte à rebours affiché.
- Notifications navigateur locales lors de la détection de nouveaux articles, avec bouton d'activation dédié et gestion des permissions.
- Mémorisation persistante des articles déjà vus pour éviter les notifications en doublon.

## [1.0.0] - 2025-02-12

### Ajouté
- Premier dashboard de veille tech/IA : agrégateur RSS avec trois catégories (Intelligence Artificielle, Dev & Web, Tech Général).
- Design "terminal / signal radar" sur mesure : palette navy/cyan/ambre, typographies Space Grotesk / Inter / IBM Plex Mono.
- Récupération des flux via rss2json.com (contournement CORS côté client).
- Bouton de rafraîchissement manuel, horodatage relatif des articles, états de chargement (skeleton) et gestion des flux indisponibles.
