# OpenClassrooms | Développeur Front-End | Projet : Booki

## Jour 1

### HTML
- ` <meta charset="UTF-8">` -> ?
- `<meta http-equiv="X-UA-Compatible" content="IE=edge">` -> ?
- Noms des `id` et `class` HTML assez longs > chercher si il y a des bonnes pratiques

### CSS
- J'ai essayé d'appliquer un style (`background-color`) à un  `<nav>`. Ca n'a pas fonctionné. <br>
En revanche ça fonctionne sur le div que j'ai rajouté à l'intérieur. <br>
Certains éléments HTML ne sont probablement pas censés être mis en forme car non affichés. A vérifier.

### GIT / GITHUB
- Documentation GIT : https://git-scm.com/docs
- GITHUB : Comprendre comment mon dossier local et le repo distant sont synchronisés
- GITHUB : Quelle différence entre HTTPS et SSH pour la connexion à Github ?
- GITHUB : Comprendre pourquoi la commande *push* fonctionne dans VS Code mais pas dans Github Desktop dans mon projet


### DIVERS
- Regarder des exemples de README.MD pour savoir quoi mettre dedans
- Me renseigner sur les licences


### NOUVEAUTES
- Emmet dans VS Code (https://code.visualstudio.com/docs/editor/emmet) <br>
`! + Entrée` pour pré-remplir la page HTML avec le doctype HTML, un head, des métadonnées<br>
`<! + Entrée` pour pré-remplir la page HTML avec le doctype HTML<br>
`.classname` pour créer un div avec *classname* comme nom de classe<br>
`#idname` pour créer un div avec *idname* comme id<br>
`ul>li*x` pour créer une liste non ordonnée avec *x* éléments dedans / testé avec des divs avec une classe commune. Super pratique pour les éléments dans ma galerie.

- Github CLI installé (https://cli.github.com/manual/index)


## Jour 2

### HTML

- ` <meta charset="UTF-8">`
>**`<meta>`** <br>
L'élément HTML <meta> représente toute information de métadonnées qui ne peut pas être représentée par un des éléments (`<base>`, `<link>`, `<script>`, `<style>` ou `<title>`) <br>
https://developer.mozilla.org/fr/docs/Web/HTML/Element/meta


> ***charset*** <br>
>Cet attribut déclare l'encodage utilisé par la page.<br>
[...] <br>
Les auteurs sont invités à utiliser UTF-8. <br>
https://developer.mozilla.org/fr/docs/Web/HTML/Element/meta

> The charset attribute specifies the character encoding for the HTML document. <br>
The HTML5 specification encourages web developers to use the UTF-8 character set, which covers almost all of the characters and symbols in the world!<br>
https://www.w3schools.com/tags/att_meta_charset.asp

- **UTF-8**
> *Universal Character Set Transformation Format1 - 8 bits*
est un codage de caractères informatiques conçu pour coder l’ensemble des caractères du « répertoire universel de caractères codés », initialement développé par l’ISO dans la norme internationale ISO/CEI 10646, aujourd’hui totalement compatible avec le standard Unicode, en restant compatible avec la norme ASCII limitée à l’anglais de base, mais très largement répandue depuis des décennies. <br>
L’UTF-8 est utilisé par près de 95,2 % des sites web en octobre 2020.

Quelques charsets :
> - ASCII
> - ISO-8859-1
> - ISO-8859-15
> - Latin-1
> - Unicode : UTF-8, UTF-16, UTF-32
> - BOM
> - ...


- **Liens utiles**
> https://www.w3.org/International/getting-started/characters <br>
> https://fr.wikipedia.org/wiki/UTF-16 <br>
http://www.steves-internet-guide.com/guide-data-character-encoding <br>


___

- `<meta http-equiv="">`

>The http-equiv attribute provides an HTTP header for the information/value of the content attribute. <br>
The http-equiv attribute can be used to simulate an HTTP response header.

- `"X-UA-Compatible" content="IE=edge"`
> Permet la compatibilité avec certaines versions d'IE.
Apparemment c'est un parti-pris, car ça sous entend devoir maintenir son site pour être compatible avec des versions futures.


https://www.w3schools.com/tags/att_meta_http_equiv.asp<br>
https://docs.microsoft.com/en-us/openspecs/ie_standards/ms-iedoco/380e2488-f5eb-4457-a07a-0cb1b6e4b4b5 <br>
https://n.survol.fr/n/x-ua-compatible-ieedge

- Chercher ce que sont les *quirks* (IE)


___
**HTML**

- **`<nav>`**
> L'élément HTML `<nav>` représente une section d'une page ayant des liens vers d'autres pages ou des fragments de cette page. Autrement dit, c'est une section destinée à la navigation dans un document (avec des menus, des tables des matières, des index, etc.). <br>
Cet élément ne possède que les attributs universels. <br>
https://developer.mozilla.org/fr/docs/Web/HTML/Element/nav


- **Attributs universels**
https://developer.mozilla.org/fr/docs/Web/HTML/Global_attributes
> Les attributs universels sont des attributs communs à l'ensemble des éléments HTML. Ces attributs peuvent donc être ajoutés sur tous les éléments (dans certains cas, les attributs n'auront aucun effet).<br>
Les attributs universels peuvent être définis sur tous les éléments HTML, y compris pour les éléments non définis dans le standard. Autrement dit, les éléments non-standards doivent pouvoir accepter ces attributs. Cela permettra au navigateur de les gérer selon certains des aspects de la spécification. Par exemple, pour un navigateur conforme, un élément ``<toto hidden>...</toto>`` sera masqué bien que ``<toto>`` ne soit pas un élément HTML valide.


> Question trouvée sur stackoverflow: <br>
*Why won't my nav element go to the center or change style?* <br>
https://stackoverflow.com/questions/19218262/why-wont-my-nav-element-go-to-the-center-or-change-style

Apparemment, pas de problème pour appliquer un style à un nav. -> Erreur de syntaxe ?

**Solution** : J'avais écrit ``#nav``, or je voulais appliquer le style à l'élément nav, pas à un élément dont l'``id="nav"`` <br>
Ca fonctionne avec : <br>
```
nav {
    color: red;
    }
```

Si on peut appliquer un style à n'importe quel élément HTML, est-ce qu'on peut mettre un style à une balise ``<head>`` ou ``<meta>`` même si ça ne se voit pas ?

### CSS

[Guide Flexbox hyper bien fait](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

A priori ça fonctionne comme la répartition des éléments dans Photoshop ou PowerPoint mais en mieux (haut, bas, gauche, droite, centré, répartir équitablement, étirer, compresser, remplir, trier, ... ) <br>

**Problème 1** 
: j'ai l'impression que d'avoir ajouté ``display: flex`` à mon élément ``nav`` l'a fait rétrécir. <br>
``width: 100%`` ne change rien mais ``width: 100px`` réduit encore la taille du menu. <br>
``width: 1000px`` ne l'augmente pas plus que ``width: 100%``<br>

**Solution**
: Après inspection de la page dans Firefox, j'avais créé un ``<div id="menu">`` dans le ``<nav>``, pensant qu'on ne pouvait pas appliquer de style directement au ``<nav>``.
En réalité, mon nav n'a jamais changé de taille, mais le div avec le background jaune si.
-> Suppression du div inutile.


**Idée 1** 
: Mettre mes 2 liens du menu (nav) dans un div et ajouter un ``justify-content: space-between`` entre le logo et le div des boutons pour les placer chacun à une extrémité du menu. <br>
-> Fait. ``<div id="navlinks">``

**Idée 2** 
: j'ai l'impression que beaucoup d'éléments de ma page sont des flex containers. Avec les classes que j'ai créé je vais devoir répéter souvent ``display: flex``. <br>
Note pour la fin du projet : voir si je peux faire des classes plus génériques pour éviter d'avoir une feuille CSS trop longue.

Grafikart | [Tutoriel CSS : px, em et rem](https://www.youtube.com/watch?v=ZV6N6w5bMDU) <br>
> *px* : valeur absolue <br>
*em* : valeur relative par rapport à l'élément parent <br>
*rem* (root em) : valeur relative par rapport à l'élément racine

***em*** :
>  “An em is a CSS unit that measures the size of a font, from the top of a font’s cap height to
the bottom of its lowest descender. Originally, the em was equal to the width of the capital
letter M, which is where its name originated.” <br> - The Principles of Beautiful Web Design<br>
Also found : **e**phe**m**eral unit


Kevin Powell | [Are you using the right CSS units?](https://www.youtube.com/watch?v=N5wpD9Ov_To)<br>
Kevin Powell | [em vs rem](https://www.youtube.com/watch?v=_-aDOAMmDHI)
> - Am I setting a font size? -> go with *rem* which are relative (to the font size of the root element) units like *em* <br>
By default the font size is 16px <br>
*rem* adapts to the user system and browser preferences.<br>
If I'm using pixels (absolute) then I may override these preferences. (not good) <br>
i.e. : user changed his default font size to a bigger one, and I force a smaller one, it's not super user friendly.

> - Am I setting a width? <br> -> a *%* coupled with ``max-width`` should work best, or ``viewport-width`` <br>
-> or *ch* unit (1 ch = approximatively the width of the number 0).
i.e : for setting a max-width on a paragraph, I could make use of *ch* because in typography we usually go for max 75 characters per line for readability.

> - Am I setting a ***height***? -> Do I really need to set a ***height***? Can I go for a ***min-height*** instead? So if the window is shrunk it won't overflow. <br>
-> %, em, rem or vw can do the job. <br>
Attention à ``viewport-height`` qui peut poser des problèmes sur terminaux mobiles (ex quand le clavier apparaît)

>- Am I setting a margin or padding? -> em or rem <br>
em: relative to parent so if the parent font-size increases, margin/padding will increase too <br>
rem: relative to root, so if the parent font-size increases, margin/padding won't change.
 

> Note on media queries : em recommended for consistency across browsers because Safari processes rem and pixels differently than other browsers. <br>
[Zell's article on media queries](https://zellwk.com/blog/media-query-units/)

Conclusion : units I should focus on: %, em, rem, a bit of ch and viewport


Liens utiles
> https://stackoverflow.com/questions/7678883/is-it-better-to-define-images-in-direct-html-or-css <br>
> [5 CSS mistakes that I see way too often](https://www.youtube.com/watch?v=iHEkRIF7zxI)<br>
> [5 mins about Media Queries](https://www.youtube.com/watch?v=2KL-z9A56SQ)<br>
> [Responsive design](https://www.youtube.com/watch?v=bn-DQCifeQQ)

Google fonts : ``<link>`` or ``@import`` : https://stackoverflow.com/questions/12316501/including-google-web-fonts-link-or-import
> For 90%+ of the cases you likely want the ``<link>`` tag. As a rule of thumb, you want to avoid ``@import`` rules because they defer the loading of the included resource until the file is fetched.. and if you have a build process which "flattens" the @import's, then you create another problem with web fonts: dynamic providers like Google WebFonts serve platform-specific versions of the fonts, so if you simply inline the content, then you'll end up with broken fonts on some platforms.

### GIT

``git commit --amend`` pour éviter de faire 2 commits quand on a oublié des fichiers https://git-scm.com/book/fr/v2/Utilitaires-Git-R%C3%A9%C3%A9crire-l%E2%80%99historique

### Problèmes à régler

- Il y a des marges autour de ma page (au moins en haut et sur les côtés) : trouver comment les retirer. -> Réglé, ajout de margin:0 et padding:0 sur tous les éléments dans le CSS.

- La border-top sur les liens du menu décale le bouton vers le bas. <br>
Solutions possible : mettre une bordure invisible/blanche sur les ``a:link, a:visited`` ou trouver un moyen de placer la bordure à l'intérieur
- J'ai importé tous les styles de Raleway, ne pas oublier d'enlever ceux qui sont inutiles.

### Historique des modifications du jour

- **CSS** Ajout de variables pour les 3 couleurs principales et pour les 2 font-weight principales

- **HTML/CSS**Ajout de commentaires dans le HTML et le CSS pour une meilleure lisibilité
- **CSS** Ajout de paramètres globaux
- **HTML/CSS**Première mise en forme des sections suivantes : Header, Welcome, Search
- **HTML/CSS**Remplacement de "hosting" par "accommodation" dans le HTML et le CSS (CTRL + SHIFT + L pour modifier en bloc tous les éléments portant le même nom)

- **CSS** Définition "en dur" une font-size par défaut à 16px, comme les spécifications demandent d'utiliser uniquement des px et des %, 
- **CSS** Définition la font-weight (identique pour h1, h2, h3) et une font-size spécifique pour h1, h2, h3 (respectivement, 22px, 20px, 18px)
- **CSS** Ajout d'une ``margin-left`` et ``margin-right`` sur le body à 3,50% (ratio mesuré sur Photoshop)
- **CSS** Ajout d'une ``margin-bottom`` de 16px (1rem par rapport à ma font-size forcée ?) en dessous de chaque section.
- **HTML** Suppression des id dans les tuiles, superflus (et super longs).

### Problèmes à régler

- La border-top sur les liens du menu décale le bouton vers le bas. <br>
Solutions possible : mettre une bordure invisible/blanche sur les ``a:link, a:visited`` ou trouver un moyen de placer la bordure à l'intérieur
- J'ai importé tous les styles de Raleway, ne pas oublier d'enlever ceux qui sont inutiles.
- La hauteur du header et du logo sont complètement arbitraires
- Balises ``article`` et ``picture`` découvertes. Documentation à lire sur le sujet. Article est une balise sémantique, probablement mieux qu'un div pour mes tuiles. Picture est a priori mieux que img car plus d'options pour les sites responsives (voir lesquelles et si utile dans le projet).

- Visuellement on dirait que le div "Les plus populaires" est un enfant de "Hébergements à Marseille" (background rouge), or ils sont enfants du même parent. Revoir la hiérarchie, et retravailler les flexbox.
