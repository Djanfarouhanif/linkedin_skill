# Posts avec performances (métriques d'engagement)

Nouveaux posts de référence, avec leurs statistiques réelles. Ce fichier sert à repérer
**quels archétypes / hooks performent le mieux** pour t'en inspirer en priorité.

**Comment lire :** plus un post a d'impressions, de likes et de commentaires, plus son
schéma (accroche, structure, CTA) mérite d'être réutilisé.

> Modèle à copier pour chaque nouveau post :
>
> ```
> ## Post — [titre court / thème]
> - **Archétype :** …
> - **Impressions :** …
> - **Likes :** …
> - **Commentaires :** …
> - **Reposts :** … (optionnel)
> - **Date :** …
>
> [texte complet du post]
> ```

---

## 🔑 Enseignements (données réelles — chiffres VÉRIFIÉS sur captures)

**Distribution des impressions par type de post :**
- Build-in-public / produit / terminal (niche) : **49 à 107**
- Storytelling universel (sécurité) : **107**
- Lancement Relay, hook universel "WhatsApp" : **1 503**
- Aphorisme métier "Un bon dev… supprime du code" (image) : **1 558**
- Débat "Backend > Frontend : le salaire" : impressions non relevées, mais **71 réactions + 23 commentaires** (record d'engagement).

> ⚠ Correction : le "100 000" évoqué de mémoire était FAUX. Le chiffre réel (capture) = **1 558**. Ne jamais réintroduire le 100k.

### Le pattern qui marche (confirmé, mais ordre de grandeur ~1 500, pas viral)
**Sujet UNIVERSEL du métier de dev, formulé en opinion tranchée / débat.** Deux sous-formats gagnants :
1. **Aphorisme en antithèse** ("Un bon dev, ce n'est pas X, c'est Y") → bonne portée (~1 558), quotable. Engagement modeste.
2. **Débat clivant** ("Backend > Frontend ?", salaires, tel outil vs tel autre) → **explosion des commentaires** (23) car les gens argumentent. C'est le meilleur levier d'ENGAGEMENT.

Pourquoi ça marche : sujet que toute la communauté dev vit → identification, débat, repartages. Pas de produit, pas de niche.

### Hiérarchie constatée
1. **Débat clivant universel** → max de commentaires/engagement. ← pour faire vivre le post et signaler l'algo.
2. **Aphorisme/opinion universelle** → bonne portée (~1 500), peu d'engagement.
3. **Storytelling universel** (sécurité) → portée moyenne (~100-1 500).
4. **Build-in-public de niche** (terminal, produit) → portée faible (50-107). Utile pour la CONVERSION, pas la croissance.

### Règles à appliquer
1. **Pour l'audience/engagement : poste des débats et opinions universelles sur le métier** (backend vs frontend, bonnes pratiques, salaires, outils, erreurs de junior…). Format court, tranché, débattable.
2. **Le sujet + le hook sont déterminants** : un sujet universel porte ~15-30× plus qu'un sujet de niche. Prouvé (1 558 vs ~70).
3. **Poser une QUESTION clivante en fin de post** booste énormément les commentaires (cf. les 23 du post salaires).
4. **Le format image "citation"** (texte de l'aphorisme en visuel) a bien marché sur "Un bon dev" — à retester.
5. **Alterne :** posts d'opinion/débat (audience) ET posts produit (conversion). Pas que du build-in-public de niche.
6. **Rester honnête sur les chiffres** : logger uniquement des valeurs vues sur capture, jamais de mémoire.

---

<!-- Chaque post généré par le skill est ajouté ici avec ses métriques. -->

---

## Post — TaskWise : "j'en ai fait la plus belle possible" (design)
- **Archétype :** Build-in-public + opinion design (semi-universelle)
- **Format :** texte + **capture de TaskWise** (le design soft UI est le héros)
- **Impressions :** _à remplir_
- **Likes :** _à remplir_
- **Commentaires :** _à remplir_
- **Reposts :** _à remplir_
- **Date :** _à remplir_
- **Angle :** assumer le cliché (to-do list = projet banal) puis le retourner en statement design → plus universel qu'un simple "regardez mon appli". Question-débat finale pour l'engagement.

Une to-do list, c'est LE projet le plus banal du monde.

Tous les devs en ont codé une.

Alors j'en ai fait la plus belle possible.

Voici TaskWise.

La plupart des apps qu'on code sont fonctionnelles. Point.

Elles marchent… mais elles ne donnent envie à personne.

Moi, je crois l'inverse :

Une app utile peut être belle.

Une app banale peut avoir du caractère.

Alors j'ai soigné chaque détail :

- Un design tout en douceur, des ombres qui donnent du relief
- Des stats claires : tâches, taux de complétion, catégories
- Des filtres fluides par statut et par priorité

Gérer sa journée. Mais avec élégance.

Parce qu'on juge une interface en 3 secondes.

Et ces 3 secondes décident si l'utilisateur reste… ou s'en va.

Le fond fait qu'un produit marche.

La forme fait qu'on l'aime.

Et toi — tu soignes le design de tes projets, ou tu t'arrêtes à « ça marche » ? 👇

---

## Post — "Le plus dur, ce n'était pas le temps réel" (galère de l'installeur)
- **Archétype :** Storytelling technique vécu + enseignement universel (livrer > construire)
- **Format :** texte + vidéo (démo Relay)
- **Impressions :** 236
- **Likes :** 8 (record pour un post "vécu" — la leçon a résonné)
- **Commentaires :** 1
- **Reposts :** 0
- **Date :** ~14 juillet 2026
- **Résultat :** meilleur post "vécu" à ce jour. 236 imp + 8 likes = un cran au-dessus du build-in-public brut (50-107). MAIS reste sous les posts d'opinion universelle (1 500+). Raison : le packaging Python est vécu et attachant, mais encore un peu technique/niche vs une vérité que TOUS les devs vivent. → Le combo idéal = vécu de Hanif + leçon la plus universelle possible.

J'ai construit une messagerie temps réel.

Le plus dur, ce n'était pas le temps réel.

Le temps réel, Django Channels et les WebSockets s'en chargent. Quelques jours, et ça tournait sur ma machine.

Le vrai cauchemar a commencé après.

Faire en sorte que ça tourne sur la machine des autres.

Parce qu'un utilisateur ne va pas :

- installer Python
- gérer des dépendances
- taper trois commandes dans un terminal

Il veut cliquer. Point.

Alors j'ai dû transformer mon projet Python en un vrai installeur Windows.

Un .exe. Sans dépendances. Qui s'installe sans droits admin. Qui rend la commande relay disponible partout.

Et là, tu découvres l'enfer des détails :

- « Windows a protégé votre ordinateur » qui fait fuir les gens
- L'app non signée qui inquiète
- Le packaging qui casse pour une raison obscure
- Tester sur une machine vierge. Encore. Et encore.

Le temps réel, c'était de l'ingénierie.

La distribution, c'était mille petits murs.

Ma leçon :

Ton code qui marche sur ta machine ne vaut rien.

Tant qu'il ne marche pas sur celle des autres.

Le plus dur, en dev, ce n'est pas de construire.

C'est de livrer.

Et toi — c'est quoi le « dernier kilomètre » qui t'a fait le plus galérer ? 👇

---

## ⭐ Post — Débat "Backend > Frontend : le salaire le prouve ?" (RECORD D'ENGAGEMENT)
- **Archétype :** Opinion / débat clivant sur un sujet universel du métier
- **Format :** texte (chiffres de salaires + liens des sources en commentaires)
- **Impressions :** _non relevé (à compléter)_
- **Réactions :** 71
- **Commentaires :** 23 🔥 (record)
- **Reposts :** 2
- **Date :** ~juillet 2026
- **Pourquoi ça marche :** sujet clivant (backend vs frontend + salaires) + question finale ("l'écart va-t-il disparaître ?") → les gens argumentent en commentaires. LE meilleur levier d'engagement à ce jour.

Structure : titre-question clivant → "j'ai regardé les chiffres" → données (salaires moyens) → analyse de l'écart (puces) → nuance ("le frontend a changé la donne") → question ouverte finale.

---

## ⭐ Post — "Un bon dev, c'est celui qui supprime du code" (aphorisme, bonne portée)
- **Archétype :** Opinion / aphorisme universel sur le métier (antithèse)
- **Format :** texte + **image "citation"** (l'aphorisme rendu en visuel)
- **Impressions :** 1 558 (chiffre vérifié sur capture — PAS 100k)
- **Réactions :** 12
- **Commentaires :** 3
- **Reposts :** 1
- **Date :** ~juillet 2026
- **Pourquoi ça a marché :** antithèse quotable "ce n'est pas X, c'est Y" + vérité universelle du métier. Bonne portée, engagement modeste. Le format image "citation" a peut-être aidé.

Texte complet :

Un bon dev, ce n'est pas celui qui écrit le plus de lignes de code.
C'est celui qui supprime du code inutile.

Depuis que j'ai compris ça, mes projets sont devenus :
✅ plus clairs
✅ plus rapides
✅ plus faciles à maintenir

Moralité : coder, ce n'est pas "ajouter toujours plus", c'est simplifier au maximum.

Et toi, tu préfères écrire ou supprimer du code ?

---

## Post — "Tu ne trouveras jamais mon mot de passe" (sécurité / mot de passe en dur)
- **Archétype :** Storytelling / insight (leçon technique)
- **Format :** texte (vidéo/capture optionnelle : screenshot flouté de l'onglet Réseau)
- **Impressions :** 144 (à 23h ; était 107 plus tôt)
- **Likes :** 2
- **Commentaires :** 0
- **Reposts :** 0
- **Date :** ~13 juillet 2026
- **Format :** texte + image "citation"
- **Note :** reste dans le couloir niche (66-144). Le sujet "sécurité / mot de passe en dur" est trop technique/étroit pour percer. Version réécrite en antithèse ci-dessous : n'a PAS fait mieux → l'idée compte plus que le format.

« Tu ne trouveras jamais le mot de passe de mon site. »

2 minutes plus tard, je l'avais.

Un ami avait généré des sites, protégés par un mot de passe.

Il était sûr de lui. Moi aussi.

Alors j'ai ouvert les outils de développement du navigateur.

Onglet Réseau. Puis le code JavaScript de la page.

Et là… le mot de passe était écrit en dur. Directement dans le code.

En clair. Visible par n'importe qui.

Je n'ai rien « hacké ». J'ai juste… regardé.

La leçon, si tu développes des sites :

Tout ce qui part dans le navigateur est public.

Le JavaScript, le HTML, les fichiers — l'utilisateur peut TOUT lire.

Un mot de passe, une clé d'API, une vérification « secrète » côté client ?

Considère que c'est déjà entre les mains de tout le monde.

La vraie sécurité se joue côté serveur. Jamais dans le navigateur.

(Rassure-toi, mon ami a corrigé depuis 😄)

Et toi — tu as déjà trouvé une faille comme ça, juste par curiosité ? 👇

---

## Post — Sécurité, VERSION RÉÉCRITE (hook antithèse) — comparaison
- **Archétype :** Storytelling + antithèse d'ouverture
- **Format :** texte + image "citation"
- **Impressions :** 170 (à 2j ; était 66 à 6h)
- **Likes :** 2 · **Commentaires :** 0 · **Reposts :** 0
- **Date :** ~13 juillet 2026
- **Leçon clé :** réécrire le même sujet avec le "format gagnant" (antithèse) N'A PAS fait décoller la portée (170, couloir niche). → Le format ne sauve pas un sujet niche. C'est l'universalité de l'idée qui compte. Hook : « La sécurité, ce n'est pas cacher un mot de passe. C'est ne jamais l'envoyer dans le navigateur. »

---

## Post ⭐ GAGNANT — "Tout le monde discute sur WhatsApp" (VERSION VIDÉO)
- **Archétype :** Storytelling → Produit (soft launch)
- **Format :** texte + **vidéo** (screencast du terminal)
- **Impressions :** 1 503
- **Likes :** 30
- **Commentaires :** 6
- **Reposts :** 0
- **Date :** ~9 juillet 2026

Hook gagnant : « Tout le monde discute sur WhatsApp. » suivi de la présentation de Relay,
accompagné d'une **vidéo de démonstration**. C'est le combo qui a explosé : hook court + vidéo.

---

## Post — "Tout le monde discute sur WhatsApp" (VERSION TEXTE SEUL)
- **Archétype :** Storytelling → Produit (soft launch)
- **Format :** texte seul (pas de vidéo)
- **Impressions :** 69
- **Likes :** 0
- **Commentaires :** 0
- **Date :** ~9 juillet 2026

⚠ MÊME hook que le post gagnant, mais **sans vidéo** → 69 impressions au lieu de 1 503.
Preuve directe de l'impact de la vidéo.

Tout le monde discute sur WhatsApp.

Moi, j'ai codé ma propre messagerie… dans le terminal.

Elle s'appelle Relay.

Un chat complet, sans jamais quitter ton terminal :

- Des salons publics
- Des messages privés
- La recherche dans tout l'historique
- L'édition et la suppression de messages
- Des statuts en temps réel
- Et même les mises à jour automatiques

Le tout en temps réel, via WebSocket. Installé en une commande, zéro dépendance à gérer.

J'ai construit ça de A à Z : le client en Python (Textual), le backend en Django + Channels, Redis et PostgreSQL derrière.

Pas un prototype. Un produit que tu peux installer maintenant.

Et ce n'est que la V1.

👉 Teste Relay ici : https://terminal-chat.hanifcode.fr/documentation

Dis-moi ce que tu en penses en commentaire — je lis tout 👀

---

## Post — "Relay est en ligne. Et ça ne fait que commencer" (avec vidéo)
- **Archétype :** Produit / momentum
- **Format :** texte + vidéo
- **Impressions :** 60
- **Likes :** 3
- **Commentaires :** 1
- **Reposts :** 1
- **Date :** ~9 juillet 2026

Relay est en ligne. Et ça ne fait que commencer.

[texte complet : voir la version "momentum" — hook plus faible que "Tout le monde discute", à retravailler]

---

## Post — Cyber Arena, hook "J'ai transformé le hacking en jeu de duel"
- **Archétype :** Feedback / validation (build in public) + CTA secondaire vers Relay V1
- **Format :** texte + vidéo (démo Relay)
- **Impressions :** 49
- **Likes :** 1
- **Commentaires :** 0
- **Date :** ~13 juillet 2026
- **Note :** hook "hacking" = sujet de niche → faible portée. La vidéo montrait Relay, pas le jeu (décalage).

J'ai transformé le hacking en jeu de duel.

Sans une seule vraie ligne de cyberattaque.

Ça s'appelle Cyber Arena.

Un duel 1v1, dans un univers de cybersécurité 100 % fictif — rien de réel, rien d'illégal. Juste un jeu.

Le principe :

Deux joueurs reçoivent le même réseau à « pirater ».

Chacun le résout de son côté, chronométré.

Des énigmes à craquer, nœud par nœud, jusqu'au coffre.

Le meilleur score grimpe au classement.

Un « chess.com du hacking fictif » : rapide, malin, rejouable.

C'est la V2 de Relay, ma messagerie qui tourne déjà dans le terminal. Même fondation. Nouvelle ambition.

Mais avant de me lancer à fond, une vraie question pour vous :

Vous joueriez à ça ?

Qu'est-ce qui vous ferait revenir… ou fuir dès la première partie ?

Je lis TOUS les commentaires. Vos retours décident de la suite 👇

👉 En attendant, testez la V1 (la messagerie) ici : https://terminal-chat.hanifcode.fr/documentation

---

## Post — Cyber Arena, hook "Tout le monde joue sur PC ou console"
- **Archétype :** Feedback / validation
- **Format :** texte + vidéo
- **Impressions :** 101 · **Likes :** 2 · **Commentaires :** 0 · **Date :** ~12 juillet 2026
- **Note :** meilleur des 3 hooks Cyber Arena (101), mais loin du 1 503 de Relay. Le sujet "jeu/hacking" touche une audience plus étroite que "messagerie/WhatsApp".

---

## Post — Cyber Arena, hook "Il y a quelques semaines, j'ai lancé Relay" (le plus lent)
- **Archétype :** Feedback / validation
- **Format :** texte + vidéo
- **Impressions :** 72 · **Likes :** 2 · **Commentaires :** 0 · **Date :** ~9 juillet 2026
- **Leçon :** hook lent/descriptif. Mais même les hooks courts (49, 101) n'ont pas fait beaucoup mieux → le hook n'était pas le seul facteur ; le sujet lui-même est plus de niche.

Il y a quelques semaines, j'ai lancé Relay : une messagerie qui tourne entièrement dans le terminal.

Aujourd'hui, je réfléchis à sa V2.

Et avant de la construire, je veux votre avis.

La V2 change tout : Relay devient un jeu.

Ça s'appelle Cyber Arena.

Un duel 1v1 qui se joue dans le terminal, dans un univers de cybersécurité 100 % fictif — rien de réel, rien d'illégal. Juste un jeu.

Le principe est simple :

Deux joueurs reçoivent le même réseau à « pirater ».

Chacun le résout de son côté, chronométré.

Des énigmes à craquer, nœud par nœud, jusqu'au coffre.

Le meilleur score grimpe au classement.

Imaginez un « chess.com du hacking fictif » : rapide, malin, rejouable.

Même fondation que Relay. Nouvelle ambition.

Mais avant de me lancer à fond, une vraie question pour vous :

Est-ce que vous joueriez à ça ?

Qu'est-ce qui vous donnerait envie de revenir… ou de fuir dès la première partie ?

Je lis TOUS les commentaires. Vos retours vont décider de la V2 👇

👉 Et si vous voulez tester la V1 (la messagerie) avant de donner votre avis, c'est par ici : https://terminal-chat.hanifcode.fr/documentation

PS : c'est encore une idée sur le papier. C'est le bon moment pour la façonner avec vous.
