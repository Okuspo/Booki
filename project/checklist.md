# Checklist projet

## Étape 1 : Mettez en place votre environnement de développement

🎯 Une fois cette étape réalisée, vous aurez :

- [x] un fichier index.html ;
- [x] un dossier “css” avec votre ou vos fichiers CSS ;
- [x] un dossier “assets” ou “images” contenant les images du projet.

📌 Recommandations

- [x] Commencez par installer VSCode.
- [x] Ajoutez la propriété CSS box-sizing.
- [x] Ajoutez les meta charset et viewport.
- [x] Ajoutez un fichier normalize.css.
- [x] Importez les polices depuis Google Font.
- [x] Ajoutez l’intégration de FontAwesome.

:warning: Points de vigilance :

- [x] Attention à bien importer vos fichiers CSS dans le “bon” ordre, autrement dit, du plus générique au plus spécifique.
Note : j'ai importé normalize.css avant style.css
- [x] Attention à bien appeler votre fichier CSS dans votre HTML, sans quoi vous ne pourrez pas utiliser le style CSS.

## Étape 2 : Découpez votre maquette à l’aide d’un papier et d’un crayon

Une fois cette étape réalisée, vous aurez :

- [x] la structure de votre code HTML ; vous pourrez vous référer à cette structure au moment de l’intégration.

📌 Recommandations
Posez-vous les questions suivantes :

- [x] Où se trouve le header ? Comporte-t-il aussi un menu de navigation ?
- [x] Où se trouve le footer ? Que comprend-il comme éléments HTML (des liens, des listes, etc.) ?
- [x] À quoi la partie “Hébergements à Marseille” ou “Les plus populaires” correspond-elle au niveau HTML ?
- [x] Quels vont être les éléments HTML composant la partie “Hébergements à Marseille” ?
- [x] Une fois que vous avez réalisé le schéma HTML de votre maquette, discutez-en avec d’autres étudiants et avec votre mentor. Cette étape va vous permettre de vous poser les bonnes questions, et de vérifier que vous n’avez rien oublié.

:warning: Points de vigilance :

- [x] Attention à ne pas réaliser un schéma trop “propre”. Ce schéma doit avant tout être simple, lisible et complet, pas besoin de le rendre très “joli”.

## Étape 3 : Intégrez le header du projet

🎯 Une fois cette étape réalisée, vous aurez :

- [x] le code HTML de l’en-tête de la page.

📌 Recommandations :
- [x] Intégrez d’abord la version desktop avant de réaliser les versions
tablette puis mobile.
- [ ] Réalisez d’abord le header pour la version desktop du projet. Une fois
la version desktop finalisée, attaquez-vous à la version tablette puis à
la version mobile.
- [x] Vous pouvez utiliser Flexbox pour réaliser le positionnement entre le
logo Booki et les parties Hébergements / Activités.

:warning: Points de vigilance :

- [x] Attention à ne pas oublier la bordure bleue qui s’affiche au survol.

- [x] Attention, la bordure bleue s’affiche au-dessus en version desktop et
en dessous en version mobile.

## Étape 4 : Ajoutez le formulaire de recherche

Vous pouvez maintenant passer à l’intégration de la barre de recherche de
la page grâce à un formulaire. Il est possible que cette étape soit un peu
plus longue que les autres.

🎯 Une fois cette étape réalisée, vous aurez : un formulaire de recherche entièrement intégré, tant pour les ordinateurs que pour les tablettes et les mobiles.

📌 Recommandations
Pour cette étape, vous allez devoir jouer avec les positionnements “absolu” et “relatif”.

- [x] Commencez par réaliser la version desktop. Essayez d’englober les trois éléments au sein d’une même balise HTML.
- [x] Intégrez d’abord le contenu HTML avant la partie CSS.
- [ ] Une fois que vous êtes satisfait de votre version desktop, réalisez la
version tablette puis la version mobile.
- [ ] Pensez à utiliser des “display: none” pour afficher ou masquer du
contenu HTML.

:warning: Points de vigilance :

- [ ] Attention au style de la barre de recherche : sur desktop, le bouton
de recherche comprend le texte “Rechercher” alors que sur mobile,
c’est une loupe.
- [ ] Attention, certains des borders radius changent en fonction de la
version, mobile ou desktop.

## Étape 5 : Ajout de la partie Filtres

Une fois cette étape réalisée, vous aurez : la partie filtre de votre projet entièrement réalisée.

📌 Recommandations :
Pour réaliser les filtres, vous n’avez pas besoin d’utiliser les positionnements “absolu” et “relatif” : vous pouvez utiliser uniquement Flexbox. Bonne nouvelle : il n’y a aucune  différence de design entre la version desktop et la version mobile.

- [x] Utilisez Flexbox aussi bien pour englober l’ensemble des filtres, qu’à l’intérieur de chacun des filtres.
- [x] Vous pouvez utiliser flex-wrap pour gérer le positionnement des éléments.
⚠ Points de vigilance :
- [x] Faites bien attention à quel moment utiliser une propriété margin plutôt que padding.
- [x] Regardez bien comment est conçu le design du filtre : la partie gauche de chacun des filtres (contenant l’icône et la couleur de fond) dépasse légèrement du cadre.
- [ ] Les valeurs des margins et des paddings sont utilisées en pourcentage et non en pixels

## Étape 6 : Réalisez la “card” présente dans “Hébergements à Marseille”

N’oubliez pas l’effet CSS demandé. Vous pouvez l’ajouter au survol et
changer, par exemple, la couleur de police.
●Si vous devez utiliser des margins et des paddings, privilégiez les
pourcentages.
●Les images doivent être intégrées via le HTML. N’oubliez pas les
attributs alt.

## Étape 7 : Réalisez la “card” présente dans “Les plus populaires"

- N’oubliez pas les border radius sur les images.
- Les images doivent être intégrées via le HTML. N’oubliez pas les attributs alt.

## Étape 8 : Gérez l’affichage des conteneurs “Hébergements à Marseille” et “Les plus populaires”

Utilisez flex et les pourcentages pour gérer les règles d’affichage. Les
ratios sont d’un tiers et de deux tiers. À vous de transformer ça en
pourcentages.
L’ordre d’affichage des deux conteneurs change en fonction de la
version : mobile ou desktop.
●Normalement, vous devriez avoir peu de modifications à apporter
aux cards que vous avez intégrées dans les parties précédentes.
●N’oubliez pas le titre, l’icône et le lien “afficher plus”.
●Les couleurs de fond s'inversent entre la version mobile et la version
desktop.

Étape 9 : Intégrez le conteneur “Activités à Marseille”

Avant d’intégrer les images, essayez de créer un conteneur par
activité et donnez-lui une classe. Cette classe va vous permettre de
jouer avec la taille, et notamment la hauteur de votre élément.
●Une fois que vous serez satisfait de la hauteur et de la disposition de
chacun des conteneurs, vous pourrez ajouter les images et les textes.

Les images doivent être intégrées via le HTML et non le CSS.
N’oubliez pas les attributs alt.

Étape 10 : Implémentez le footer

Si vous utilisez des `ul` pour réaliser les liens, vous avez par défaut
un padding-left qui s’applique. Pensez à l’enlever.
●Faites bien attention à respecter le positionnement du footer et
notamment le “À propos”, avec le reste de la maquette.

Concentrez vos efforts sur les erreurs remontées. Vous pouvez
regarder les warnings, mais vous n’êtes pas obligé de les traiter.
●Faites attention au nommage du code. Vous pouvez le réaliser en
anglais ou en français, mais évitez de mixer les deux langues.
●Utilisez le kebab case, par exemple `.main-wrapper`. C’est LA
convention CSS la plus répandue.
●N’oubliez pas que seul Flexbox est autorisé. Vous ne devez pas utiliser
Grid.
●Seuls les pixels et les pourcentages sont autorisés. Utilisez les pixels
pour les margins, les paddings et les pourcentages pour les widths.