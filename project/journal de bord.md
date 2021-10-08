# OpenClassrooms | Développeur Front-End | Projet : Booki

# Index

- [Jour 1](#j1)
- [Jour 2](#j2)
- [Jour 3](#j3)
- [Jour 4](#j4)


 # <a name="j1"> Jour 1</a>

### HTML
- ` <meta charset="UTF-8">` -> ?
- `<meta http-equiv="X-UA-Compatible" content="IE=edge">` -> ?
- Noms des `id` et `class` HTML assez longs > chercher si il y a des bonnes pratiques

### CSS
- J'ai essayé d'appliquer un style (`background-color`) à un  `<nav>`. Ca n'a pas fonctionné. <br>
En revanche ça fonctionne sur le div que j'ai rajouté à l'intérieur. <br>
Certains éléments HTML ne sont probablement pas censés être mis en forme car non affichés. A vérifier.

### GIT / GITHUB
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


# <a href="j2">Jour 2</a>

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

- **HTML/CSS** Ajout de commentaires dans le HTML et le CSS pour une meilleure lisibilité
- **CSS** Ajout de paramètres globaux
- **HTML/CSS** Première mise en forme des sections suivantes : Header, Welcome, Search
- **HTML/CSS** Remplacement de "hosting" par "accommodation" dans le HTML et le CSS (CTRL + SHIFT + L pour modifier en bloc tous les éléments portant le même nom)

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


# <a href="j3"> Jour 3</a>

Flexbox :

**display: inline-flex**

> If we didn’t want div elements to be block-level elements, we would use display: ``inline``. Flexbox, however, provides the ``inline-flex`` value for the display property, which allows us to create flex containers that **are also inline elements**.\
[Codecademy - Learn intermediate CSS](https://www.codecademy.com/courses/learn-intermediate-css/)


>In HTML programming, a block-level element is any element that starts a new line (e.g., paragraph) and uses the full width of the page or container. A block-level element can take up one line or multiple lines and has a line break before and after the element.
https://www.computerhope.com/jargon/b/block-level-element.htm

> ``display: inline-flex`` does not make flex items display inline. It makes **the flex container display inline**. That is the only difference between ``display: inline-flex`` and ``display: flex``. A similar comparison can be made between display: ``inline-block`` and ``display: block``, and pretty much any other display type that has an inline counterpart.\
\
**There is absolutely no difference in the effect on flex items**; flex layout is identical whether the flex container is block-level or inline-level. In particular, the flex items themselves always behave like block-level boxes (although they do have some properties of inline-blocks). You cannot display flex items inline; otherwise you don't actually have a flex layout.\
It is not clear what exactly you mean by "vertically align" or why exactly you want to display the contents inline, but I suspect that flexbox is not the right tool for whatever you are trying to accomplish. Chances are what you're looking for is just plain old inline layout (display: inline and/or display: inline-block), for which flexbox is not a replacement; flexbox is not the universal layout solution that everyone claims it is (I'm stating this because the misconception is probably why you're considering flexbox in the first place). \
\
[Q&A stackoverflow](https://stackoverflow.com/questions/27418104/whats-the-difference-between-displayinline-flex-and-displayflex)

> When we add display: flex, we are really defining display: **block** flex. <br>
https://www.smashingmagazine.com/2018/08/flexbox-display-flex-container/
MERCI !!!!

https://discuss.codecademy.com/t/whats-the-difference-between-display-flex-and-display-inline-flex/370020

https://css-tricks.com/multiple-class-id-selectors/



# <a href="j4">Jour 4</a>

## CSS cool stuff

"Text is always king"

`::before` and `::before` pseudo elements<br>
https://www.youtube.com/watch?v=zGiirUiWslI<br>
https://www.youtube.com/watch?v=xoRbkm8XgfQ<br>
https://www.youtube.com/watch?v=QFjqxVMwIl8<br>


New properties and attributes discovered :
- `position-absolute`
- `counter-increment`
- `isolation: isolate`
- `overflow: hidden`
- `inset` : https://developer.mozilla.org/fr/docs/Web/CSS/inset (expérimental)
- `z-index`
- `opacity`
- `mix-blend-mode` -> Comme dans Photoshop
- `mix-blend-mode: multiply`
- `mix-blend-mode: screen`
- `gradient`, linear, radial,conic, repeating..., https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/radial-gradient()

[How to create a duotone effect and mix blend modes](https://egghead.io/lessons/css-use-css-pseudo-elements-and-mix-blend-mode-to-create-a-duotone-style-effect)


> Box shadow: <br>
> https://www.youtube.com/watch?v=u6Rur7G8HNY <br>
https://tobiasahlin.com/blog/how-to-animate-box-shadow/ <br>
https://codepen.io/kevinpowell/pres/abmOeoG <br>
> A mettre dans ma page !!!
> En bref : on crée un calque avec l'ombre déjà présente, et on la toggle avec ``transition: opacity 1s ease;``<br>
> Cas 1 : on crée une box-shadow
> Différence : l'ombre est déjà calculée, on change juste son opacité<br>
> Différence dans l'exemple : 32ms rendering + 18ms painting contre 20ms rendering + 2ms painting<br>


Emmet : go to matching pair (pratique pour mon wrapper)

___
> **Padding as a void** In the initial CSS implementation by Netscape Navigator 4, padding was sometimes a void.  What I mean is, you could give an element a background color, and you could set a border, but if you adding any padding, in some situations it wouldn’t take on the background color, allowing the background of the parent element to show through.  Today, we can recreate that effect like so: 

    border: 3px solid red;
    padding: 0.5em;
    background-color: cornflowerblue;
    background-clip: content-box;
https://meyerweb.com/
___

## Markdown

Trouver un système de catégories en markdown/html pour récupérer tous les éléments correspondant et les exporter vers un autre markdown (ex : "CSS_stuff.md", "Emmet_shorhands.md")<br>
Possibilité d'utiliser une classe HTML dans le markdown mais besoin d'un script pour extraire les paragraphes correspondants et les écrire dans les autres markdowns.<br>
-> a voir quand j'aurai appris javascript/node.js

___

## CSS 

Explication et exemples d'imbrication de propriétés CSS (nesting)<br>
https://www.pierre-giraud.com/html-css-apprendre-coder-cours/imbrication-heritage-etendu/ <br>


### Parenthèse "UI/UX après visite du site de Pierre Giraud" 
 La croix pour fermer la pop-up qui s'affiche sur sa page est située **en bas à gauche** de la pop-up.<br>
D'ordinaire elle soit situé en haut à droite dans les fenêtres Windows, en haut à gauche sur Linux et Mac. <br>

**Question naïve :** est-ce qu'il y a des études menées en ergonomie sur les mouvement du bras lorsqu'on déplace la souris ?
<br> Observation perso : faire un mouvement d'adduction de l'épaule a l'air de demander moins d'effort que de faire un mouvement d'adbduction, et le mouvement me semble plus précis. <br>
(Le problème se pose moins dans le cas d'une fenêtre en plein écran car la souris arrive en butée en haut à droite de l'écran.)

Pourquoi les boutons de contrôle d'une fenêtre sont situés en haut et pas en bas, alors qu'ergonomiquement ça semble plus confortable d'y accéder quand ils sont en bas.

-> Peut être parce qu'en bas il y a le menu démarrer ou le dock et que ça évite de cliquer accidentellement dessus.<br> 
-> Ou peut être pour dissuader de fermer la page/ pop-up. :'D <br>
-> Ou c'est une question de sens de lecture, et qu'on considère que les contrôles (Ficher, Edition,... [x] Fermer la page) précèdent le contenu.

Liens connexes: https://ux.stackexchange.com/questions/23733/what-is-better-window-buttons-on-the-left-os-x-or-on-the-right-windows

> **I think this is one of those things where you should do what the user expects.** <br>
> What do they expect? Well that's sometimes the tricky thing to figure out. Eye movement studies have been done in excess to determine the best placement for the most important call-to-action buttons. And users often start in the upper-left hand corner. On the other hand, these window buttons are so ubiquitous and so familiar that they shouldn't require unnecessary thought. If a user is accustomed to an OS with the buttons on a certain side of the screen they will naturally be looking for them in that spot. Past experience is going to be the dominant factor in what the user expects.<br>
So for example, if your audience is composed of 90% Windows users, I think you should absolutely put these buttons in the upper-right. Windows users will naturally look in the upper-right hand corner for these buttons because that's what they've been trained to do.<br>
Or better yet, if you can adopt the built-in window controls (title and button placement) of the target OS, then it takes this decision out of your hands and the buttons will always be where the user expects.<br> 
https://ux.stackexchange.com/questions/7/what-is-the-important-aspect-to-consider-when-deciding-where-windows-interaction

-> Problème de ce raisonnement, si on dispose les éléments par rapport à ce que les utilisateurs ont l'habitude de voir, on ne peut rien faire évoluer. <br>
Point intéressant du post : on place les éléments par rapport au regard/sens de lecture (début : haut/gauche) / lecture en Z,...
donc "ergonomie" pas au sens anatomique (mouvement d'épaule, du bras, de la main).
<br> Pistes à explorer : 
- Les mouvements de curseur des joueurs de FPS. (ex: Razer et son app de heatmaps et de tracking de curseur) 
- Des études d'ergonomie sur le placement des éléments fréquemments utilisés, dans une page web ou une app.

___

## CSS 
NESTING 
https://www.alsacreations.com/tuto/lire/545-Comprendre-l-heritage-et-la-parente-des-styles-CSS.html

Il y a un héritage "natif" concernant les balises ``<a>`` et ses enfant (pseudo classes ``:link`` ``:visited``, ``:hover``, ``:active``)

    .menu li {
        propriétés
    }
éléments li dont le parent à la classe "menu"

    li .menu {
        propriétés
    }
éléments de la classe menu dont le parent est un ``<li>``

    li, .menu {
        propriétés
    }
pas d'héritage ici (avec la virgule), c'est juste pour grouper les propriétés d'éléments sans rapport, comme dans mon CSS :

    html, body {
        width: 100%;
    }
<br>
    
    li.menu {
        propriétés
    }

Elément `<li>` qui possède la classe ``menu``

Aucune explication sur cette page du sélecteur d'imbrication `&` ni de la règle `@nest`.

[CSS Nesting Module - W3C First Public Working Draft, 31 August 2021](https://www.w3.org/TR/css-nesting-1)

    table.colortable td {
    text-align:center;
    }
    table.colortable td.c {
    text-transform:uppercase;
    }
    table.colortable td:first-child, table.colortable td:first-child+td {
    border:1px solid black;
    }
    table.colortable th {
    text-align:center;
    background:black;
    color:white;
    }

Nesting allows the grouping of related style rules, like this:

        table.colortable {
    & td {
        text-align:center;
        &.c { text-transform:uppercase }
        &:first-child, &:first-child + td { border:1px solid black }
    }
    & th {
        text-align:center;
        background:black;
        color:white;
    }
    }

https://stackoverflow.com/questions/4564916/nesting-css-classes

**Le nesting n'est pas encore possible en vanilla CSS. Seulement avec Sass et Less (chercher ce que c'est).**

Problème rencontré avec la section Activités à Marseille

- J'ai essayé de mettre les 6 cartes dans 1 seul container flex avec comme propriétés :

    flex-flow: column-wrap;
    justify-content: space-between;

Les 2 grandes cartes font 100% de la ``height:990px`` du container, et les plus petites cartes s'empilent bien.

Problème : l'inversion du main et du cross axis fait que si on réduit la largeur de la page, les cartes débordent.


Test 2 : j'ai rajouté 2 divs, chacun englobe 2 petites cartes.
Le container flex est maintenant en :

    flex-wrap: wrap;
    justify-content: space-between;

les divs "colonne" en :

    flex-direction: column;
    justify-content: space-between;

Nouveau problème : les tags ``<a>`` autour des ``<article>`` ne sont pas des éléments flex. <br>
J'aimerais éviter de mettre une propriété flex à des ``<a>`` car ça ne fait pas de sens. <br>
Mettre les ``<a>`` dans les ``article`` ne résoud pas le problème car l'``<article>`` est aussi un container flex.

     <section id="activities_results">
           
        <h1>Activités à Marseille</h1>

        <div class="ar_gallery">
        
        ...
        
        <div class="ar_column">
           <a href="#">                 
                <article class="ar_card small_3">
                    <h2>Notre-Dame-de-la-Garde</h2>
                    <img src="assets/activites/4_small/notre_dame_de_la_garde.jpg"></img>     
                </article>
            </a>
        
            <a href="#">
                <article class="ar_card small_4">
                    <h2>Parc Longchamp</h2>
                    <img src="assets/activites/4_small/parc_longchamp.jpg"></img>
                </article>
            </a>
        </div>



**To do**

- PAGE : Revoir toutes les margin-bottom et les regrouper
- PAGE : vérifier les règles en doublons avec l'ajout de normalize.css (box-sizing,...)
- PAGE : vérifier si ma méthode d'import de FontAwesome est bonne (CDN ?)
- NAV : ajouter des liens vers les sections au menu
- SECTION SEARCH FORM : mettre en forme la barre de recherche et les filtres, passer l'icone "i" en `::before` du `<p>`
- SECTION SEARCH FORM : Trouver une meilleure solution que du padding à la mano pour l'icone FA child.
- SECTION CITY RESULTS : Ajouter une ancre au h1
- SECTION CITY RESULTS : ajouter des ombres aux cartes
- SECTION CITY RESULTS : revoir les design des cartes proprement et passer en revue les propriétés CSS
- SECTION CITY RESULTS : Afficher plus : lien à rajouter et font-weight à changer
- ASIDE MOST POPULAR RESULTS : bien placer l'icone par rapport au titre (la passer en `::after` ?)
- ASIDE MOST POPULAR RESULTS : revoir l'alignement des détails de la carte
- ASIDE MOST POPULAR RESULTS : ajouter des ombres aux cartes
- SECTION ACTIVITIES RESULT : ajouter les liens aux cartes
- SECTION ACTIVITIES RESULT : ajouter une ancre au h1
- SECTION ACTIVITIES RESULT : le wrap fait passer les cartes sous le footer !! <br>
probablement lié au fait que j'ai sorti le footer du wrapper pour qu'il fasse 100% du body width.
- SECTION ACTIVITIES RESULT : Le wrap des 2 cartes d'un coup parce qu'elles sont dans la même colonne est très moche.
- FOOTER : Espace entre les titres et les ``<ul>``
