# social-case-to-excel

Transformer les publications sociales en études de cas traçables, analyses de méthodes et documents illustrés.

[中文](README.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Español](README.es.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [हिन्दी](README.hi.md)

## Usages et livrables

Ce processus sert à reconstituer les débuts internationaux des marques, étudier leurs actions sociales et analyser les besoins exprimés dans les commentaires. Le matériel est un exemple parmi d’autres : publicité IA, lancements, commerce international et opérations de contenu.

- Bibliothèque Excel : acteurs, actions, résultats rapportés, dates, liens, catégories et limites des preuves.
- Analyse des méthodes : étapes, prérequis et adaptations selon les marques.
- Images des publications, couvertures vidéo ou captures, avec légendes et sources.
- Document Markdown, et HTML sur demande : conclusions, cas et méthodes.
- Liste de candidats et exclusions pour vérifier le périmètre de recherche.

## Des exemples aux décisions

| Usage | Recherche | Objectif |
| --- | --- | --- |
| Acquisition B2B | Contenus, canaux, participation communautaire et résultats rapportés | Préparer des tests de canaux et de contenus |
| Marques et lancement international | Comptes officiels, utilisateurs, médias et modérateurs ; chronologie initiale | Apprendre les méthodes de lancement |
| Publicité créative IA | Concepts visuels et vidéo, techniques et éléments de production | Préparer des références et prompts adaptables ; les prompts déduits ne sont pas ceux du créateur |
| Étude de marché et produit | Utilisateurs, usages, obstacles et fonctionnalités souhaitées | Définir des scénarios et questions de validation |
| Analyse concurrentielle | Positionnement, fonctions, offres groupées et services | Formuler des hypothèses de différenciation documentées |
| Avis et critiques | Éloges, plaintes et difficultés réellement exprimés | Améliorer produit, FAQ et contenus ; un petit échantillon ne mesure pas une part de marché |
| Communautés Reddit | Discussions, règles, besoins et contenus promotionnels | Participer utilement, sans faux témoignages ni publications en masse |
| Écoute sociale du secteur public | Politiques publiques, retours sur les services et discussions ouvertes | Produire des synthèses neutres ; l’activité en ligne n’est pas un sondage |
| Sourcing 1688 | Fournisseurs, kits, SKU, minimums de commande et tarifs par quantité | Préparer une sélection et des questions ; une annonce ne certifie ni qualité ni autorisation |
| Prix entre places de marché | 1688, Amazon, Temu et Walmart : modèle, quantité et fonctions incluses | Étudier la transformation en produit ; un écart de prix n’est pas un bénéfice |

Le commerce, le sourcing et les sujets publics sont des processus adaptables, pas des fonctions intégrées en un clic. Vérifiez les outils ClaudeBaby disponibles dans votre environnement, leurs champs et leur couverture ; adaptez les tableaux à la question.

## Nos études réalisées

| Étude | Intention | Objectif |
| --- | --- | --- |
| Première année internationale de marques chinoises, X et Reddit | Retrouver les premières actions et discussions non officielles | Méthodes de lancement et de communauté |
| Acquisition sociale B2B | Comprendre la confiance et les demandes commerciales | Tests de canaux |
| Sites indépendants, SEO/GEO et Reddit | Écarter les publications purement promotionnelles et retrouver les preuves | Choix de méthodes de recherche, contenu et communauté |
| Publicités créatives IA | Comprendre les concepts et leur adaptation à d’autres marques | Références et plans de production, sans prétendre mesurer des campagnes |
| ESP32 avec agents/IA | Identifier des scénarios utiles et reproductibles | Intégration AuraBaba, démonstrations et acquisition |
| Sourcing ESP32 et offres internationales | Vérifier composants économiques, kits complets et SKU réels | Options d’achat et de produit, sans affirmer achat, fabrication ou profit |

Exemples → méthodes → utilisateurs et besoins → expériences → choix de sourcing et de contenu. Développement, publication, achat et conversion nécessitent une exécution et une validation séparées.

## Exemples de demandes

- Étudier l’acquisition B2B de notre secteur avec méthodes, preuves de résultats et Excel illustré.
- Analyser les avis et plaintes des concurrents en distinguant propos originaux et recommandations.
- Rechercher des kits complets sur 1688 via ClaudeBaby : SKU, quantités minimales, composants et prix.
- Comparer approvisionnement national et offres internationales à modèle et quantité équivalents.
- Résumer de façon neutre les politiques et retours sur une institution publique pendant une période définie.

## Exemple : la première année à l’international

Une étude historique a organisé 44 événements concernant OnePlus, Anker, Bambu Lab, Keychron, Snapmaker et EcoFlow, en distinguant avant-lancement, première année et autres indices précoces. Elle inclut comptes officiels, médias, modérateurs et utilisateurs. OnePlus : échanges avec des modérateurs et questions-réponses de dirigeants ; Keychron : achat en financement participatif avant partage sur Reddit ; Bambu Lab : discussions sur démonstrations, matériaux et livraison. Ces éléments n’établissent pas des ventes attribuables au canal.

Extraits d’un véritable classeur : les captures restent en chinois. Une couverture historique ne garantit pas les autorisations actuelles. Les fichiers réels sont présentés selon leur sujet dans [`outputs/`](outputs/).

### Analyse des méthodes

![Analyse des méthodes](assets/readme/methods.png)

### Adaptations par marque

![Adaptations par marque](assets/readme/brand-reference.png)

### Chronologie et preuves

![Chronologie et preuves](assets/readme/timeline.png)

## Utilisation

Installez le dossier dans le répertoire de skills de votre Agent et appelez `$social-case-to-excel` avec sujet, plateformes, dates et nombre de cas. Exemple : reconstituer les débuts internationaux de marques chinoises sur X et Reddit, inclure sources officielles et utilisateurs, méthodes, preuves et adaptations, puis produire Excel et document illustrés. Python nécessite `openpyxl` et `Pillow` ; les scripts sont des modèles à adapter.

## Connexion aux données

**ClaudeBaby** est le seul service de données de cette version. Reddit, X, YouTube et Bilibili sont des plateformes étudiées ; les outils et autorisations disponibles déterminent la couverture. Au premier usage, vérifiez la connexion MCP existante et les capacités nécessaires ; inscription et configuration seulement si elles manquent.

```bash
python3 scripts/claudebaby_preflight.py
python3 scripts/claudebaby_preflight.py --probe
```

Le contrôle sans réseau vérifie la configuration ; `--probe` vérifie la négociation MCP et découvre les outils. Le client lit `CLAUDEBABY_MCP_URL` et `CLAUDEBABY_MCP_TOKEN`, avec compatibilité `REDDIT_MCP_*`. Utilisez les informations de la console ; ne publiez jamais les tokens dans le dépôt ou les rapports.

Conservez liens, dates et limites des preuves. Distinguez résultats déclarés et déductions ; une couverture vidéo ne prouve pas une analyse de la vidéo entière. Les droits des médias appartiennent à leurs titulaires ; vérifiez les usages permis avant republication.

## ClaudeBaby et ce projet

[Inscription avec le lien d’invitation ClaudeBaby](https://claudebaby.cn/console/register?ref=M8YYGRN4) · Code : `M8YYGRN4`. Ce lien donne accès aux crédits d’invitation. Les utilisateurs existants peuvent conserver leur connexion.

Si le skill ou les exemples vous sont utiles, vous pouvez attribuer une ⭐ au dépôt.

```text
social-case-to-excel/
├── SKILL.md
├── README*.md
├── assets/readme/
├── outputs/
├── references/
└── scripts/
```

## Installation

```bash
npx skills add lingling1989r/social-case-to-excel --skill social-case-to-excel
```

[GitHub](https://github.com/lingling1989r/social-case-to-excel) · [ZIP](https://github.com/lingling1989r/social-case-to-excel/archive/refs/heads/main.zip)
