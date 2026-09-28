# Projets de Hanif (base de connaissances pour les posts)

Ce fichier catalogue les projets de Hanif. Quand un post concerne un projet, s'appuyer sur sa
fiche ici pour être **techniquement exact** (stack, fonctionnalités, état d'avancement).
Ne jamais inventer une techno ou une feature : si ce n'est pas dans la fiche, demander à Hanif.

---

## Relay — Messagerie en temps réel dans le terminal

- **Statut :** V1 livrée et installable (Windows). Documentation en ligne.
- **Doc / téléchargement :** https://terminal-chat.hanifcode.fr/documentation
- **Pitch une ligne :** une app de messagerie temps réel entièrement utilisable depuis le terminal, sans navigateur — expérience inspirée de Claude Code, mais dédiée au chat.

### Vision
Communiquer en temps réel sans quitter le terminal, via une interface TUI (Text User Interface)
élégante et légère. Multiplateforme visé : Windows, Linux, macOS.

### Public cible
Développeurs, administrateurs système, équipes techniques, étudiants — des gens qui vivent dans le terminal.

### Fonctionnalités V1 (déjà là)
- **Auth** : inscription, connexion, déconnexion, JWT + refresh auto. Identifiants mémorisés, reconnexion auto, saisie du mot de passe masquée.
- **Profil** : username, avatar (option), statut, dernière connexion.
- **Salons** : créer / rejoindre / quitter / lister (`/create`, `/join`, `/leave`, `/channels`).
- **Messagerie** : messages instantanés, historique, heure d'envoi, édition (`/edit`), suppression (`/del`).
- **Messages privés** : `/dm <user>`, historique privé.
- **Présence** : en ligne / hors ligne / occupé / absent (`/status`).
- **Recherche** : par utilisateur, salon ou message (`/search`).
- **Notifications** : quand on t'écrit, te mentionne, ou rejoint un salon.
- **Autres** : `/users` `/online` `/history` `/whoami` `/clear` `/logout` `/exit`, mises à jour auto au démarrage.
- **Raccourcis** : Ctrl+N (salon), Ctrl+K (recherche), Ctrl+L (effacer), Ctrl+Q (quitter), Ctrl+H (historique).
- **Install** : installeur Windows par utilisateur, sans droits admin, zéro dépendance à gérer ; la commande `relay` devient dispo partout.

### Stack technique
- **Client (TUI)** : Python 3.13+, **Textual**, Rich, prompt_toolkit, websockets, httpx, Typer.
- **Backend** : **Django**, Django REST Framework, **Django Channels**, Redis, PostgreSQL, JWT.
- **Temps réel** : WebSocket sécurisé (WSS) via Django Channels + Redis.
- **Déploiement** : Docker, Nginx, Gunicorn, Daphne, HTTPS/WSS.
- **Archi** : Client → WSS → Django Channels → (Redis + PostgreSQL).

### Objectifs de perf
Connexion < 1 s · envoi message < 100 ms · viser 5 000 utilisateurs connectés simultanément · reconnexion auto après coupure.

### Roadmap (angles de futurs posts)
- **V2** : réactions 👍❤️🔥, réponses à un message, pièces jointes (images/vidéos/audio), emojis, GIF, sondages.
- **V3** : appels audio/vidéo, partage d'écran, IA intégrée, traduction auto, plugins, bots, chiffrement de bout en bout, sync multi-appareils.

### Angles storytelling exploitables
- "Une messagerie dans le terminal" (contre-intuitif → bon hook).
- Le défi technique du temps réel (WebSockets, Django Channels, Redis).
- Les coulisses : de l'idée au PRD au produit installable.
- Build in public : chaque version = matière à post.
- (Éviter d'axer sur "autodidacte" — mettre en avant le produit et la compétence technique.)

---

## Cyber Arena CLI — Jeu de duel compétitif dans le terminal (= Relay V2)

> **⚠ Lien clé :** Cyber Arena CLI EST la **V2 de Relay** — son évolution, pas un projet isolé.
> La plateforme Relay grandit : de la messagerie au terminal (V1) → vers le jeu au terminal (V2),
> sur **la même fondation** (même stack + même pipeline de déploiement).
> Fil narratif fort à exploiter : *"j'ai bâti une fondation (Relay V1), maintenant je la fais
> évoluer vers quelque chose de plus ambitieux (V2)."*
> Toujours présenter les deux comme **un seul produit qui évolue**, une progression du build in public.
> NB : la roadmap "V2/V3" listée dans la PRD messagerie de Relay ci-dessus était le plan
> messagerie d'origine ; la vraie direction que prend Hanif pour la V2, c'est Cyber Arena.

- **Statut :** en conception (PRD MVP rédigé). Pas encore construit. Réutilise toute l'infra de Relay.
- **Commande de lancement :** `cyberarena`
- **Pitch une ligne :** un jeu de duel 1v1 jouable au terminal, dans un univers de cybersécurité **100 % fictif et simulé** — un "chess.com du hacking fictif".

### Positionnement clé
- **PAS** un FPS temps réel façon PUBG/COD (impossible/frustrant au terminal).
- **Duel d'énigmes / d'intrusion, asynchrone et tour-par-tour** : rapide, malin, rejouable, classé.
- **Asynchrone** : les 2 joueurs affrontent le même défi sans être en ligne en même temps (règle le démarrage à froid).
- **Server-authoritative** : le serveur génère et valide tout, le client n'affiche/n'envoie que des actions → **anti-triche par conception**. C'est LE principe non négociable.

### Le mode MVP : "Breach Duel" (1v1 async)
- Les 2 joueurs reçoivent **le même réseau fictif** (même seed), le résolvent seuls et chronométrés. Meilleur score = gagne l'ELO.
- **Réseau** : petit graphe de 6-10 nœuds (routeur, serveur, base de données, coffre…), chaque nœud a un **verrou = mini-énigme**. Objectif : atteindre le nœud `vault` et l'exfiltrer.
- **Commandes in-game** : `scan`, `move <node>`, `crack <node> <réponse>`, `hint <node>`, `exfiltrate`, `status`.
- **3 types de verrous** (énigmes procédurales, 100 % serveur) : Code (deviner un nombre à 4 chiffres, plus/moins), Motif (compléter une suite logique), Déchiffrement (César/substitution simple).
- **Score** = base − actions − temps − indices. Calculé et stocké côté serveur.
- **ELO** classique + **leaderboard** global + historique des manches.

### Stack technique (réutilise Relay)
- **Client** : Python 3.13+, Textual, Rich, websockets, httpx, Typer.
- **Backend** : Django + DRF + Django Channels + Redis + PostgreSQL + JWT.
- **Temps réel** : WSS. WebSocket `/ws/duel/` (events : matched, state, result, elo_update).
- **Déploiement** : réutilise tout le pipeline Relay (Docker, Nginx, TLS, installeur Windows zippé, vérif de version).

### Modèle de données MVP
Player (elo défaut 1000), Match (seed, status), MatchEntry (score, actions, time_ms). Les énigmes ne sont pas stockées : régénérées depuis le seed (déterministe).

### Philosophie MVP (angle de post fort)
- But : **le plus petit jeu jouable et fun possible**, pour prouver que 2 personnes s'amusent avant de construire un jeu live-service complet.
- **Critère de réussite unique** : 2 personnes jouent 3-4 duels d'affilée et ont envie de recommencer.
- **Hors périmètre assumé** (§10) : clans, saisons, cosmétiques, coop, store… → ligne rouge anti scope-creep. (Bots d'entraînement = seul "MVP+" possible.)

### Angles storytelling exploitables
- Réutiliser l'infra d'un projet (Relay) pour en lancer un autre plus vite.
- Le server-authoritative / anti-triche par conception (angle technique fort).
- La discipline du MVP : définir ce qu'on ne construit PAS (§10).
- "Un jeu de hack dans le terminal" (hook contre-intuitif).
- Build in public : du PRD au playtest "fun / pas fun".

---

## TaskWise — To-do list web au design soigné (soft UI / neumorphism)

- **Statut :** construit (au moins une V1 fonctionnelle vue en capture). _À compléter : en ligne ? URL ? open source ?_
- **Pitch une ligne :** un gestionnaire de tâches web élégant. Slogan : « Gérez votre journée avec élégance. »
- **L'angle central = le DESIGN.** Interface soft UI (neumorphism) : ombres douces, relief, esthétique apaisante. C'est le point de différenciation que Hanif met en avant ("style parfait").
- **Fonctionnalités vues :** dashboard avec stats (tâches totales, taux de complétion, catégories), création de tâche, catégories (ex. Personnel), priorités (basse/…), filtres par statut (Tout / À faire / En cours / Terminé) et par priorité, recherche, édition/suppression, dates.
- **Stack :** _à préciser par Hanif_ (probablement Angular côté front vu son profil — à confirmer, ne pas inventer).
- **Angles de posts :** le design comme différenciateur ("une to-do list, mais belle"), soigner l'UX même sur un projet banal, le détail qui fait la différence, avant/après d'un design.


---

## TogoExplore — Plateforme web de découverte des sites touristiques du Togo

- **Statut :** en développement. Partie API (Django REST Framework) en cours, plusieurs briques déjà en place. _À compléter : en ligne ? URL ? open source ? front final ?_
- **Pitch une ligne :** une plateforme web pour découvrir, noter et partager les sites touristiques du Togo — valoriser le patrimoine togolais en le rendant visible en ligne.

### Fonctionnalités déjà en place (côté API)
- API des sites touristiques (fiches).
- Système de **favoris** pour les utilisateurs connectés.
- Système d'**avis et de notes**.
- Sérialisation des données (DRF serializers).
- Gestion des **permissions et de l'authentification**.
- **Documentation automatique** de l'API (Swagger / OpenAPI).

### Stack technique
Python · Django · Django REST Framework · SQLite · HTML/CSS · Git/GitHub
_(À confirmer : base de prod prévue — PostgreSQL ? front Angular ou templates Django ?)_

### Angles storytelling exploitables
- **Le meilleur hook (validé par l'usage) :** l'absence de présence numérique du patrimoine togolais → "cherche *que visiter au Togo* sur Google, tu ne trouves presque rien". Problème concret + fierté locale = hook large.
- Le patrimoine comme sujet universel (tout le monde a déjà cherché où partir), le produit n'affleure qu'en preuve.
- La valeur vient des utilisateurs (avis/notes), pas du fondateur → angle communauté.
- ⚠ **À éviter :** la liste de features + "ça me permet d'apprendre et de progresser". Posture de débutant, et c'est le schéma qui plafonne à ~80 impressions (cf. TaskWise).

---

## Défi 2 « Environnement » — Laboratoire d'IA du Togo (Togo AI Lab)

- **Statut :** livré. Participation au défi data du **Togo AI Lab** sur l'accès à l'électricité, les énergies propres et la protection des forêts au Togo.
- **Dashboard :** https://bilalidjanfarou-svg-defi2-environnement-dashboardapp-0nrabd.streamlit.app
- **Code source :** https://github.com/bilalidjanfarou-svg/defi2_environnement
- **Pitch une ligne :** une analyse croisée de 6 jeux de données togolais, livrée sous forme de tableau de bord interactif orienté recommandations.

### Données & constats (chiffres fournis par Hanif — ne pas arrondir ni inventer)
- **6 jeux de données croisés** : électricité, météo, pollution, sources d'énergie, forêts.
- **Écart d'accès à l'électricité : 71,5 points** entre urbain (**96,5 %**) et rural (**25 %**).
- **89,4 % des ménages** dépendent du bois ou du charbon pour la cuisson.
- **Émissions de GES : 87,7 %** pour agriculture/forêt/terres, contre **6,2 %** pour le secteur énergétique.
- **Savanes et Kara** = zones prioritaires (température élevée + faible couverture forestière + retard d'électrification).

### Livrable technique
Tableau de bord interactif **Python + Streamlit** : cartographie des forêts classées, filtres géographiques, analyse croisée orientée recommandations.

### Angles storytelling exploitables
- **Le meilleur angle (utilisé) :** le flip contre-intuitif — on croit que la pollution vient des usines, au Togo elle vient des terres et des forêts (87,7 % vs 6,2 %) → et la cause remonte à la cuisson au bois, donc au manque d'électricité rurale. Chaîne causale lisible, punchline « une histoire de cuisine ».
- L'inégalité 96,5 % / 25 % dans un même pays (angle social fort).
- Le data pour la décision publique : « un chiffre dans un CSV ne change rien, un chiffre explorable si ».
- Montre une corde de plus que le web : data / analyse / Streamlit.

---

## LLM maison — Modèle de langage entraîné from scratch (19M paramètres)

- **Statut :** en cours d'entraînement (sept. 2026). _À préciser par Hanif : architecture (GPT-like ? nb de couches ?), tokenizer, langue du dataset, source du corpus, objectif final (démo ? produit ? article ?)._
- **Taille du modèle :** **19 millions de paramètres**.
- **Dataset :** **~300 millions de caractères**.
- **Environnement d'entraînement :** **Google Colab, tier GRATUIT** — GPU NVIDIA T4 (~15 Go de VRAM), RAM système ~12-13 Go, disque `/content` ~70-100 Go (temporaire, non garanti), session jusqu'à ~12 h, Google Drive 15 Go.
- **Contrainte clé :** 15 Go de VRAM largement suffisants pour 19M de paramètres ; le vrai risque est la **volatilité de la VM** (disque effacé, session coupée) → checkpoints sur Drive.

### Angles storytelling exploitables
- ⭐ **Ressource gratuite (archétype 8)** : « on peut entraîner un LLM sans acheter de GPU » — hook universel (coût) + surprise + preuve par SON usage.
- Les limites honnêtes de Colab Free (le disque temporaire, rien n'est garanti) → crédibilité.
- Build in public de l'entraînement : courbe de loss, premiers textes générés (bons ET ratés), coût réel = 0.
- Ce qu'on apprend en construisant un LLM plutôt qu'en appelant une API.
