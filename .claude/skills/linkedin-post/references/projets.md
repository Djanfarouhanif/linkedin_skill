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
