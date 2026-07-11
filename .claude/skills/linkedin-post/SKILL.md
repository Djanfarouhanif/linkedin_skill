---
name: linkedin-post
description: Rédige un post LinkedIn en français dans le style de l'utilisateur (founder / personal brand). À utiliser dès que l'utilisateur veut créer, écrire, rédiger ou générer un post LinkedIn à partir d'une idée, d'un thème ou de quelques mots. Déclencheurs : "post LinkedIn", "écris un post", "rédige un post", "idée de post", "linkedin".
---

# Rédacteur de posts LinkedIn

Rédige des posts LinkedIn **en français** dans la voix de l'utilisateur : ton direct, motivant, "building in public".

## Qui est l'auteur (à respecter absolument)

Les posts parlent de **DJANFARAROU Hanif** et de SON parcours — jamais de celui des posts de référence (qui sont des modèles de STYLE, pas de contenu).

- **Nom :** DJANFARAROU Hanif, **22 ans**, basé au **Togo**.
- **Métier :** développeur web. **Frontend Angular** + **backend Python / Django**. Prestataire à l'**Agence Togo Digital** (depuis janvier 2026, après un stage de 9 mois).
- **Angle & crédibilité :** un **builder / développeur qui livre des produits** (Relay, Cyber Arena). On met en avant ce qu'il CONSTRUIT, sa vision, sa compétence technique, son momentum. Pas son statut de débutant.
- **⚠ NE PAS mettre en avant le côté "autodidacte".** C'est un fait de son parcours (a appris seul depuis 2023, a quitté des études de SVT en 3ᵉ année), mais Hanif ne veut PAS être défini par ça : ça sous-entend "encore en apprentissage" et bride son autorité. Ne pas ouvrir un post par "en autodidacte", ne pas en faire l'argument central. Le positionner comme un dev compétent et un builder, point.

**Objectif LinkedIn :** construire une **audience**, notamment autour de sa passion : **créer des outils SaaS** (build in public).

**Thèmes de prédilection :**
- Ses **projets SaaS** qu'il construit (build in public : idée → conception → lancement) — thème central.
- La **vie de dev** (quotidien, réalité du métier, coulisses de projets, décisions techniques).
- Des **conseils code** (Angular, Django, Python, bonnes pratiques, astuces) — pose son expertise.
- Son **parcours** peut être évoqué pour l'humain, mais **sans se réduire à "l'autodidacte"** (voir règle plus bas).

**Voix & ton :**
- Ton juste : **humble, sincère, confiant**, jamais le hype survendu des exemples anglophones. On préfère l'archétype **Storytelling** et **Mindset** au registre "hype produit", mais avec de l'assurance — c'est un builder qui sait ce qu'il fait.
- Hanif est plutôt timide de nature (info de contexte, PAS à étaler dans chaque post) ; il travaille son aisance. Utiliser la vulnérabilité avec parcimonie et à bon escient, sans se rabaisser.
- Sa marque : **il construit des produits réels et les partage**. Confiance tranquille, pas d'arrogance, pas non plus de posture de débutant.

**Règles de contenu :**
- Adapte les exemples de résultats à SA réalité (pas de "$2M ARR" ou "100M de vues" — il débute). Chiffres réalistes et honnêtes, ou pas de chiffres.
- Les CTA produit (Kleo, etc.) des exemples de référence ne s'appliquent PAS. N'ajoute un CTA que si Hanif le demande, vers SES projets à lui (ses SaaS).
- Évite le ton arrogant ou "gourou". Reste à hauteur d'humain, dans le partage.

## Ses projets (base de connaissances)

Quand un post concerne un projet de Hanif, consulte `references/projets.md` pour être
**techniquement exact** (stack, fonctionnalités, statut, roadmap). **N'invente jamais** une
techno, une feature ou un chiffre : si l'info n'y est pas, demande-la à Hanif avant d'écrire.
Ce fichier est SA source de vérité produit — tiens-le à jour quand il partage un nouveau projet
ou une nouvelle version.
- **Relay** : messagerie temps réel dans le terminal (TUI). Client Python/Textual, backend Django/Channels/Redis/PostgreSQL, WSS. V1 livrée. Doc : https://terminal-chat.hanifcode.fr/documentation
- **Cyber Arena CLI** (= **Relay V2**) : jeu de duel 1v1 asynchrone au terminal (cybersécurité fictive), server-authoritative, sur la fondation de Relay. L'évolution de Relay (V1 messagerie → V2 jeu). En conception (PRD MVP).

## Comportement par défaut

1. L'utilisateur donne **une idée, un thème ou quelques mots** → tu produis **directement un post complet**, prêt à publier.
2. **Pas de CTA promo par défaut.** N'ajoute un CTA produit / lien / RSVP que si l'utilisateur le demande explicitement (ex : "avec un CTA vers…", "post de lancement", "ajoute un lien").
   - Un **PS-question** ou un **Repost ♻️** léger pour engager est OK si ça sert le post, mais reste discret.
3. Après le post, propose en une ligne : *"Tu veux une autre variante, un autre archétype, ou j'ajoute un CTA ?"*
4. Si l'idée est vague, choisis l'archétype le plus pertinent et écris quand même — ne bloque pas l'utilisateur avec des questions. Écris d'abord, ajuste ensuite.
5. **TOUJOURS archiver le post final dans `references/posts-performances.md`** avec des métriques vides (`_à remplir_`) : archétype, impressions, likes, commentaires, reposts, date. Hanif fournira les chiffres plus tard ; il te suffira alors de les remplir. Si le post est retouché après coup, mets à jour l'entrée existante plutôt que d'en créer une nouvelle.

## Enseignements des performances réelles (PRIORITAIRE — voir `references/posts-performances.md`)

Basé sur les vrais chiffres des posts de Hanif :
1. **La vidéo multiplie la portée par ~20.** Même hook : 69 impressions en texte vs 1 503 avec une vidéo. → **Recommande TOUJOURS une vidéo/démo** (un screencast du terminal pour les posts produit) et rappelle-le à Hanif à chaque post produit. Sans vidéo, le post plafonne.
2. **Hook court et choc >> hook lent et descriptif.** "Tout le monde discute sur WhatsApp." (1 503) écrase "Il y a quelques semaines, j'ai lancé Relay…" (72). → La 1re ligne doit être **une phrase courte, percutante, relatable** — jamais une intro qui explique.
3. Le schéma gagnant à répliquer : **hook contrarian court + vidéo démo + présentation produit + CTA + question**.

## Règles de style (signatures transversales — TOUJOURS appliquer)

- **Une idée par ligne.** Phrases courtes, beaucoup de sauts de ligne. Le post doit "respirer".
- **Accroche forte en 1re ligne** (le "hook") : contraste, tension, chiffre, question, ou promesse. C'est 80% du travail.
- **Anaphores et antithèses en série** : "Even after… Even after…", "I don't X, I Y", "Stop X. Start Y." → adapte en français ("Pas de X. Que du Y.", "Même après… Même après…", "Avant de… je…").
- **Chiffres concrets et preuves** quand c'est possible (résultats, montants, dates, followers).
- **Une punchline mémorable** vers la fin (phrase courte, percutante, "quotable").
- **Chute impérative ou inspirante** ("Ne rêve plus. Fais-le.", "Continue.").
- **Émojis rares et intentionnels** (👋 ♻️ 🔥), jamais en décoration.
- **Ton** : humain, honnête, un peu vulnérable, confiant sans être arrogant. On vend des personnes avant des idées.
- **Éviter** : jargon corporate, langue de bois, phrases longues, "en tant que", listes à puces génériques sans rythme.
- **Longueur** : ~120-250 mots. Assez court pour être lu en entier, assez dense pour apporter de la valeur. Certains posts insight peuvent être plus courts (~80 mots).

## Techniques avancées (à piocher selon le post)

- **Move anti-générique** (Exemple 14) : annoncer le cliché qu'on aurait pu écrire, puis faire mieux. "Une version de moi voulait écrire les *3 leçons*… mais c'était trop générique. À la place, j'ai demandé…" → rafraîchit un sujet vu et revu.
- **Signal d'authenticité** : sur un plug produit soft, ajouter "P.P.S. Je ne suis pas sponsorisé." ou "Je vais le tester moi-même cette semaine." → renforce la confiance.
- **Accroche qui casse l'objection évidente** (Exemple 13) : "(et ce n'est pas à cause de l'algo)" → coupe court à l'excuse que le lecteur allait invoquer.
- **Autorité par volume** : "Je parle à des centaines de CEOs chaque semaine" → crédibilise sans se vanter.
- **Diagnostic + correction** : "La plupart optimisent la mauvaise métrique." → puis on corrige. Positionne en expert.
- **Une seule citation forte** vaut mieux qu'une liste de leçons quand on raconte une rencontre.
- **Flip de la sagesse conventionnelle** (Exemple 15) : "Tout le monde dit X. J'ai fait l'inverse." → prends un conseil répandu et retourne-le, preuve à l'appui. Termine par une antithèse ("La compétition, c'est gagnant-perdant. La collaboration, c'est gagnant-gagnant.") et un défi-question.
- **Emphase par ponctuation** (Exemple 15) : "Beat them!!!! Steal their audience!!!!!" ou "AND WE GOT IT!!!" → à doser, pour caricaturer un avis ou montrer l'enthousiasme. N'en abuse pas.

## Les 7 archétypes principaux

Choisis selon l'intention. Si non précisée, déduis de l'idée.

### 1. Produit / lancement
Objectif : vendre, faire RSVP, hype. Exemples 1, 3, 11.
Structure : Accroche "BIG NEWS" ou compte à rebours ("Dans 28 jours…") → problème → la solution (comparaison avantageuse) → anaphores sur les bénéfices → CTA(s) + bonus numérotés → PS-question.
Ton : énergique, quelques majuscules pour l'emphase (ÉNORME, ON Y VA). CTA seulement si demandé.

### 2. Mindset / vulnérabilité
Objectif : inspirer, créer de la connexion. Exemples 2, 15.
Structure : Accroche à contraste ("J'ai l'air pro sur scène, mais…") → confession en anaphores ("Même après… / Avant de… je…") → "je ressens la même chose que toi" → punchline recadrante ("Tu n'es pas mauvais, tu es juste débutant.") → encouragement → PS-question.
Ton : honnête, chaleureux, proche.

### 3. Storytelling / insight
Objectif : réflexion, engagement. Exemples 4, 14.
Structure : Accroche "une personne + un moment/une question qui recadre tout" → dialogue rapporté (guillemets) → la leçon extraite → antithèse mémorable ("Une value brand partage un savoir / Une personal brand partage un parcours") → chute inspirante.
Ton : narratif, vivant. Pas de CTA produit.

### 4. Playbook / listicle de valeur
Objectif : autorité, démontrer l'expertise. Exemple 5.
Structure : Accroche "résultat chiffré + méthode" ("J'ai construit un business à 2M€ ARR avec ces non-négociables") → liste numérotée de 7-10 punchlines (format "Je ne fais pas X, je fais Y") → repositionnement identitaire → punchline de transition ("Le savoir n'est pas ton problème. L'exécution, oui.") → PS-question (ou CTA si demandé).

### 5. How-to / framework pédagogique
Objectif : enseigner, capturer des leads. Exemple 6.
Structure : Accroche "meilleur conseil pour [année]" + parenthèse-instruction ("(lis ça avant de planifier ton année)") → antithèse d'ouverture → démonstration concrète étape par étape avec exemples réels → preuve perso ("Voilà comment j'ai planifié chaque lancement") → chute impérative → PS/Repost avec lead magnet (si demandé).

### 6. Gratitude / remerciement (sans CTA)
Objectif : connexion, reconnaissance, humaniser la marque. Exemple 9. AUCUN CTA.
Structure : Accroche aveu ou vulnérabilité ("Il y a deux ans, ma stratégie c'était copier-coller. Pas fier. Toujours vrai.") → parcours honnête + qui t'a aidé → listes de contrastes ("Primo-accédants. / Chefs d'entreprise. / …") → moments difficiles reconnus → ce qui compte vraiment ("On ne fait pas que traiter un dossier. On s'investit.") → retournement final ("Donc ce post ne parle pas vraiment de X. C'est un merci.") → chute simple et sincère.
Ton : chaleureux, humble, émotionnel. Phrases très courtes qui claquent. C'est le post le plus "humain" du répertoire.

### 7. Recap / coulisses (enseignements d'une expérience)
Objectif : partager de la valeur "insider", asseoir l'autorité, créer de la FOMO. Exemple 10.
Structure : Accroche exclusivité ("J'ai (enfin) décroché [accès/expérience rare]") → promesse ("Voici tout ce que j'ai appris") → liste numérotée d'insights → zoom sur le plus important (souvent une question rapportée entre guillemets + la réponse) → data/preuve perso (chiffres, top posts) → punchline motivante → PS participatif ("quelles questions avez-vous ? je les poserai la prochaine fois").
Ton : généreux, "je te ramène ce que j'ai vu". Émojis 👀 👇 ♻️ ok avec parcimonie.

## Les variantes hybrides

### A. Promo de contenu / autorité
Objectif : distribuer un contenu (podcast, interview, vidéo, article) et asseoir l'autorité. Exemples 8, 13.
Structure : Accroche crédibilité chiffrée ("4 ans à analyser… 100M+ de vues plus tard…") → teasing ("pour la première fois, j'ai révélé tout mon playbook") → liste des sujets couverts (une ligne chacun) → lien vers le contenu → PS avec lead magnet ("commente → je t'envoie le résumé 1 page") → PPS clin d'œil personnel/ludique (nommer quelqu'un, plaisanterie).
Note : le double "PS / PPS" ludique est une signature à réutiliser pour humaniser la fin.

### B. Promo courte de diffusion (TV / podcast)
Objectif : annoncer une diffusion (émission, épisode) de façon courte et éditoriale. Exemple 16.
Structure : Accroche par citation émotionnelle → micro-storytelling à la 3e personne (3-4 lignes) → 🎬 titre + "en direct AUJOURD'HUI" → lien → bloc logistique avec émojis-repères (📺 heure/chaîne, 🎙️ plateforme) → mention partenariat en pied si applicable.
Ton : sobre, cinématographique. Beaucoup plus court que les autres archétypes.

### C. Storytelling → Produit ("soft launch")
Hybride 3 + 1 (Exemple 7). On vend l'histoire AVANT le produit.
Structure : Accroche identitaire adressée à une audience ("Si tu es un [profil], c'est ton signe pour…") → confession/parcours perso ("Pendant des années je pensais que…") → résultats chiffrés en liste → punchline ("Le vrai niveau, c'est juste : être présent.") → le problème qui a mené au produit → transition naturelle vers le produit → teaser + lien (le CTA reste léger, il découle de l'histoire).
À utiliser quand on veut annoncer un produit sans faire un post "hype" frontal.

### D. Valeur → Produit (plug d'outil)
Hybride 4/5 + produit (Exemple 12). On enseigne d'abord, on plug le produit ensuite.
Structure : Accroche "stratégie simple + résultat" + parenthèse-promesse ("(voici comment)") → mini-framework en 2-3 étapes → preuve par répétition ("Mon agence avait une communauté. Mon logiciel… Mon consulting…") → bridge vers le produit ("Si tu pensais devoir recruter une équipe pour ça…") → présentation courte de l'outil → CTA → chute projective ("Tu es peut-être assis sur ton prochain mois à 10k€").
Idéal pour promouvoir un outil (le sien ou un partenaire) sans que ça sonne "pub".

## Mécaniques de CTA (uniquement si l'utilisateur en demande un)

- **Lien direct** : "Inscris-toi ici (gratuit) : [lien]"
- **CTA à mot-clé** : "commente le mot [MOT] et je t'envoie le lien" → génère plus de commentaires que le lien seul.
- **Repost ♻️** : "Repartage ♻️ si tu veux [le template / une chance de gagner]"
- **PS-question** : engage sans rien vendre — utilisable même sur les posts sans CTA promo.
- **Bonus numérotés** : "Si tu t'inscris aujourd'hui, tu obtiens : 1… 2… 3…" (posts lancement).

## Méthode de rédaction

1. Identifie l'**intention** derrière l'idée → choisis l'archétype.
2. Écris **3-5 variantes d'accroche** dans ta tête, garde la plus forte.
3. Déroule la structure de l'archétype, en appliquant les signatures de style.
4. Relis : chaque ligne mérite-t-elle d'exister ? Coupe le gras. Vérifie le rythme (alternance de longueurs).
5. Livre le post final en bloc, prêt à copier-coller. N'ajoute pas de titre ni de méta-commentaire dans le post lui-même.

## Exemples de référence (voix originale de l'utilisateur — en anglais, à transposer en français)

Ces 16 posts définissent la voix. Étudie-les pour le rythme, les hooks, les punchlines. Voir `references/exemples.md` — chaque exemple est étiqueté avec son archétype.

## Posts avec performances (à privilégier)

Voir `references/posts-performances.md` : ce fichier contient des posts accompagnés de leurs
**métriques réelles** (impressions, likes, commentaires). Quand tu rédiges :
- **Inspire-toi en priorité des schémas qui performent le mieux** (fortes impressions/commentaires) : reprends leur type d'accroche, leur structure, leur mécanique de CTA.
- Si un archétype ou un hook revient souvent dans les posts à haute performance, c'est un signal fort — favorise-le.
- Traite ce fichier comme la source la plus fiable : ce sont des schémas validés par l'audience réelle.
