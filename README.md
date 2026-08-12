Veille — Dashboard de veille tech & IA

Un dashboard mono-fichier, sans build, sans backend, pour suivre l'actu tech, IA et dev en un coup d'œil — flux RSS agrégés en direct, design "signal radar", installable comme une app sur mobile.

Créé par [`<Dylan/>`](https://kancica.com/dylan/) — développeur full stack basé à Cotonou 🇧🇯.

---

## Fonctionnalités

- **3 catégories de veille** : Intelligence Artificielle, Dev & Web, Tech Général
- **Flux bilingues** : chaque catégorie combine une source anglophone et une source francophone
- **Auto-refresh horaire** avec compte à rebours affiché
- **Notifications navigateur locales** dès qu'un nouvel article est détecté
- **Articles marqués comme lus** au clic, grisés et mémorisés durablement
- **Résilient aux pannes réseau** : timeouts, retries automatiques, état d'erreur clair
- **Installable en PWA** sur iPhone/Android (ajout à l'écran d'accueil)
- **Zéro dépendance, zéro build** : un seul fichier `index.html`, tourne partout

## Aperçu technique

| **Stack** | HTML / CSS / JavaScript vanilla |
| **Flux RSS** | via [rss2json.com](https://rss2json.com) (contournement CORS côté client) |
| **Stockage** | persistance locale des articles lus / vus |
| **Polices** | Space Grotesk, Inter, IBM Plex Mono (Google Fonts) |
| **Dépendances** | aucune |

## Démarrage rapide

Aucune installation nécessaire :

```bash
git clone https://github.com/gwalabsbj/veilledashboard.git
cd veilledashboard
```

Puis ouvre simplement `index.html` dans ton navigateur — ou héberge-le gratuitement sur **GitHub Pages** :

1. Va dans **Settings → Pages** de ton repo
2. Source : branche `main`, dossier `/ (root)`
3. Ton dashboard sera accessible à `https://gwalabsbj.github.io/veilledashboard/`

## Installer comme une app (iPhone / Android)

1. Ouvre l'URL du dashboard dans Safari (iOS) ou Chrome (Android)
2. Appuie sur **Partager** → **Sur l'écran d'accueil**
3. Lance l'app depuis l'icône plutôt que depuis le navigateur pour des notifications plus fiables

> **Limite connue sur iOS** : Apple restreint fortement les notifications en arrière-plan pour les apps web. Elles fonctionnent tant que l'app est ouverte ou récemment utilisée, mais pas de façon garantie si elle reste fermée plusieurs jours. Pour du vrai push fiable en toutes circonstances, il faudrait un backend dédié (voir [Roadmap](#-roadmap)).

## Personnaliser les flux

Toute la configuration se trouve en haut du `<script>`, dans l'objet `CATEGORIES` :

```javascript
const CATEGORIES = [
  {
    id: 'ia',
    label: 'Intelligence Artificielle',
    feeds: [
      { name: 'MIT Tech Review', url: 'https://www.technologyreview.com/topic/artificial-intelligence/feed' },
      { name: 'Actu IA', url: 'https://www.actuia.com/feed/' }
    ]
  },
  // ...
];
```

Ajoute, retire ou remplace n'importe quel flux RSS en modifiant ce tableau — aucune autre modification nécessaire.

## Roadmap

- [ ] Backend léger (Node.js) pour du vrai push notifications même app fermée
- [ ] Catégorie dédiée à l'actu tech francophone/africaine
- [ ] Mode sombre / clair
- [ ] Export des articles lus en CSV

## Contribuer

Les PR sont bienvenues ! Pour proposer un nouveau flux RSS, une correction de bug ou une amélioration :

1. Fork le repo
2. Crée une branche (`git checkout -b feature/ma-feature`)
3. Commit tes changements
4. Ouvre une Pull Request

## Licence

Distribué sous licence MIT.
