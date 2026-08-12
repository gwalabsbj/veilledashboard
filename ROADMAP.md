# Roadmap

Ce document liste les évolutions envisagées pour le dashboard de veille. Rien n'est figé — les priorités peuvent bouger selon les retours et contributions de la communauté.

Légende : 🔴 pas commencé · 🟡 en réflexion / prototype · 🟢 en cours de dev

---

## 🔔 Notifications & synchronisation

- 🔴 **Backend de push notifications** — petit serveur (Node.js) qui interroge les flux côté serveur et pousse des notifications même quand l'app est fermée, via Web Push (VAPID). Résout la limite actuelle liée aux restrictions iOS sur le web en arrière-plan.
- 🔴 **Fréquence de refresh configurable** — choisir 15 min / 30 min / 1h / 3h au lieu d'une heure fixe.
- 🔴 **Digest quotidien par email** — un résumé du matin envoyé automatiquement, pour ceux qui préfèrent ne pas être notifiés en continu.
- 🔴 **Monitoring de la santé des flux** — badge d'alerte si un flux RSS est down ou n'a pas publié depuis longtemps, pour repérer les sources mortes.

## 📚 Contenu & sources

- 🔴 **Catégorie "Communauté FR/Afrique"** — sources tech francophones et ouest-africaines dédiées.
- 🔴 **Interface de gestion des flux** — ajouter/retirer une source RSS depuis l'UI plutôt qu'en éditant le code.
- 🔴 **Recherche et filtres par mot-clé** — retrouver un article déjà vu, filtrer par source.
- 🔴 **Système de tags automatiques** — détection de mots-clés (ex : "OpenAI", "React", "Rust") pour filtrer rapidement.
- 🔴 **Résumé automatique des articles** — génération d'un résumé court par IA pour scanner plus vite sans quitter le dashboard.
- 🔴 **Favoris / articles à lire plus tard** — distinct du marquage "lu", pour mettre de côté ce qu'on veut approfondir.

## 🎨 UX & personnalisation

- 🔴 **Mode clair / sombre**
- 🔴 **Réorganisation des catégories** (drag & drop) et catégories personnalisées créées par l'utilisateur
- 🔴 **Vue compacte / vue détaillée** — basculer entre liste dense et cartes avec plus de contexte
- 🔴 **Raccourcis clavier** — navigation façon lecteur RSS (j/k pour naviguer, Enter pour ouvrir, r pour marquer lu)
- 🔴 **Export des articles lus en CSV/JSON**

## 📱 Mobile & PWA

- 🔴 **Manifest PWA complet** (icône, nom, couleurs) pour une installation plus propre sur l'écran d'accueil
- 🔴 **Mode hors-ligne** via service worker — consulter les derniers articles chargés sans connexion
- 🔴 **Widget iOS/Android** — aperçu rapide sans ouvrir l'app (nécessite passage en app native ou Shortcuts)

## 🤝 Communauté & contribution

- 🔴 **Multi-utilisateur avec configs partagées** — permettre à d'autres de dupliquer facilement leur propre instance avec leurs flux
- 🔴 **Bibliothèque de flux prêts à l'emploi** — un fichier `feeds-library.json` avec des flux vérifiés par catégorie/langue, que la communauté peut enrichir via PR
- 🔴 **Thèmes visuels alternatifs** — d'autres directions graphiques proposées par la communauté, sélectionnables

## ⚙️ Infra & qualité

- 🔴 **Remplacement de rss2json.com par un proxy CORS auto-hébergé** — pour ne plus dépendre des limites de l'API gratuite
- 🔴 **Tests basiques** (validation des flux, parsing) pour éviter les régressions
- 🔴 **CI GitHub Actions** — vérifier automatiquement que les flux RSS configurés répondent toujours

---

## Comment proposer une idée

Ouvre une [issue](../../issues) avec le préfixe `[idée]` dans le titre, ou directement une Pull Request si tu as déjà une implémentation. Toute contribution est bienvenue, du petit fix au feature complète.
