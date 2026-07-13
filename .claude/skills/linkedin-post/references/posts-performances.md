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

## 🔑 Enseignements (données réelles — mis à jour au fil des posts)

Basé sur 6 posts de Hanif (juillet 2026). **Honnêteté statistique : échantillon petit, compte jeune → chiffres volatils. Ne pas surinterpréter.**

**Distribution réelle des impressions :** 49, 60, 69, 72, 101, **1 503**.
→ La plupart des posts font **50-100 impressions** (normal pour un compte qui démarre). Le **1 503 est un outlier isolé**, pas un résultat reproductible pour l'instant.

1. **⚠ La vidéo N'EST PAS un ×20 fiable.** Conclusion initiale corrigée : les posts vidéo font 49-101 (comme le texte à 69). La vidéo ne nuit pas, mais ne garantit RIEN à elle seule. Ne plus la vendre comme la solution miracle.
2. **Ce qui distingue le post à 1 503 :** (a) c'était le **lancement** de Relay (nouveauté), (b) hook **ultra-relatable** ("WhatsApp" = tout le monde), (c) probable pic d'engagement précoce. Les hooks plus étroits ("jouer sur console", "le hacking") touchent moins de monde → portée plus faible.
3. **Piste la plus solide :** la **relatabilité du hook** (un sujet que TOUT LE MONDE vit) semble compter plus que le format. À tester davantage.
4. **Leviers réels pour un compte jeune** (au-delà du contenu) : régularité, répondre vite à chaque commentaire, commenter d'autres posts avant/après publication, publier quand l'audience est active, donner du temps. Un post viral isolé ne fait pas une tendance.
5. **Besoin de plus de données** avant de fixer des règles. Continuer à logger chaque post ici.

---

<!-- Chaque post généré par le skill est ajouté ici avec ses métriques. -->

---

## Post — "Tu ne trouveras jamais mon mot de passe" (sécurité / mot de passe en dur)
- **Archétype :** Storytelling / insight (leçon technique)
- **Format :** texte (vidéo/capture optionnelle : screenshot flouté de l'onglet Réseau)
- **Impressions :** _à remplir_
- **Likes :** _à remplir_
- **Commentaires :** _à remplir_
- **Reposts :** _à remplir_
- **Date :** _à remplir_
- **Hypothèse testée :** sujet universel (sécurité) + démonstration de compétence → devrait mieux porter que les posts "terminal" de niche.

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
