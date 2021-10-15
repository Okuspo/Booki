# Soutenance Projet 2 : Booki

## Support personnel en préparation à la visio 

### 1. Rappel du contexte du projet  (2 minutes)

- Réalisé : création d'un prototype du site de l'entreprise Booki, dans le cadre d'un stage dans cette entreprise.
- Comment : en intégrant des maquettes en HTML / CSS d'un design fait par Loïc.
- Pourquoi : ce prototype servira de base de code pour le reste du développement du projet.
- Pour qui : projet réalisé à la demande de Sarah, la CTO de Booki (ma responsable).

### 2. Présentation du rendu visuel du projet (5 minutes)

Présenté sur Firefox via live-server

- Version desktop (3 minutes)
- Version tablette (1 minute)
- Version mobile (1 minute)

### 3. Présentation du code (5 minutes)

#### 3.1 Arborescence du repo (30 secondes)

- index.html
- dossier CSS / fichiers CSS (normalize.css, style.css)
- dossier assets (images, logo, favicon)

#### 3.2 Structure HTML (1 minute)

- Head : Metadonnées et imports (ordre des fichiers CSS, imports Google Fonts, FontAwesome, favicon)

- Sections : Header / Menu de navigation, Section 1: Welcome, S2: Search, S3: Accomodation results / S4: Activity results / Footer

#### 3.3 Structure CSS (1 minutes)

- Survol de la structure du fichier style.css via l'index (global / sections / media queries)
- Focus 1 : règles globales (variables, base des cartes, animations)
- Focus 2 : règles spécifiques aux media queries

### 4. Points de complexité (2.30 minutes)

#### Point de complexité 1 : animation de box-shadow

En Material Design, les ombres sont complexes : 1 élément a plusieurs box-shadows. (génère un rendu plus réalistes qu'une ombre simple)

Problème posé :
Appliquer une animation sur la propriété box-shadow peut poser des problèmes de performance.

Le problème est amplifié si le terminal est peu performant (mobile), plusieurs box-shadows doivent être animées simultanément, ou encore si plusieurs animations sont actives en même temps (ce n'est pas le cas ici).

Solution proposée :

- Définir une box-shadow initiale (attributs multiples) pour un élément de base (carte)
- Définir une box-shadow finale (attributs multiples) pour un pseudo-élément lié à la carte
- Appliquer une transition sur l'opacité du pseudo-élément (0 -> 1) plutôt que de modifier les attributs de box-shadow.

#### Superposition des pseudo-éléments et des liens hypertextes

Complexité générée par l'utilisation de pseudo-éléments par rapport à l'empilement des couches sur l'axe z (objectif : garder les liens au niveau le plus haut pour être cliquables)

Solution proposée : appliquer un z-index supérieur à mes lien.

- Par défaut : mes éléments HTML ont un niveau 1
- Par défaut : mes pseudo-éléments ont un niveau 2
- Modifié : mes liens ont un niveau 3

### 5. Bilan du projet (2 minutes)

#### Résultat

Le site est fonctionnel et semblable aux maquettes fournies.

#### Réalisation

- Difficultés rencontrées sur quasiment tous les aspects du projet (notions d'HTML, aucunes connaissances préalables en CSS).
- Quelques difficultés de lecture de la maquette. Notamment pour les espaces (qu'est-ce qui relève du padding, de la margin, d'un espacement flex, qu'est-ce qui est fixe ou variable).

#### Points d'amélioration

**Spécificité des sélecteurs**
J'aurais pu éviter certains ID en me servant davantage des combinateurs. J'ai préféré les ID car ça m'a aidé à me repérer.

**Etat des filtres**
Les filtres pourraient avoir un état "activé".
On peut imaginer que plusieurs filtres soient activés en même temps
Leur apparence doit montrer si un filtre est actif ou non.

**Responsivité**

On doit pouvoir réduire le nombre de règles spécifiques aux media queries, notamment en utilisant :

- Des dimensions relatives : em et rem. Evite de surcharger les valeurs des tailles de font en pixel par endroits, permet de définir des margin et paddings en fonction de la taille locale de la font.
- Une grid pour la partie Activité : évite de créer des sous containers flex tout en conservant la disposition relative des objets
