# OpenClassrooms | Développeur Front-End | Projet : Booki

## Index

- [Spécifications fonctionnelles](#fonc_spec)
- [Spécifications techniques](#tech_spec)
- [Jour 1](#j1)
- [Jour 2](#j2)
- [Jour 3](#j3)
- [Jour 4](#j4)
- [Jour 5](#j5)
- [Jour 6](#j6)
- [Jour 7](#j7)
- [Jour 8](#j8)

___

## <a id="fonc_spec"> Spécifications fonctionnelles</a>

- Les usagers pourront rechercher des hébergements dans la ville de
leur choix. Le champ de recherche est un champ de saisie, le texte
doit donc pouvoir être édité par l’utilisateur. Il faut englober ce
champ dans un formulaire pour que ce dernier soit valide auprès du
W3C. La partie recherche ne doit pas être fonctionnelle. **OK**
- Chaque carte d’hébergement ou d’activité devra être cliquable dans
son intégralité (pas uniquement le titre). Pour l’instant, les liens sont
vides. On peut utiliser un attribut `href=”#”` pour simuler la
présence d’un lien.
- Les filtres doivent changer d’apparence au survol. Je te laisse décider
de l’effet approprié, je n’ai pas encore eu le temps de me pencher
dessus. Par contre, ils ne doivent pas être fonctionnels. **TO DO**
- Les textes “Hébergements” et “Activités”, situés dans l’en-tête, sont
des liens. Ils doivent mener respectivement vers la section
“Hébergements à Marseille” et “Activités à Marseille”. **TO DO**

## <a id="tech_spec"> Spécifications techniques</a>

- Deux maquettes ont été réalisées : l’une desktop et l’autre mobile. Le
site devra être également adapté aux formats tablette. Pour les
tablettes, nous sommes libres de faire les adaptations nécessaires. Il
est important qu’aucun élément ne soit coupé, et que le texte ait
une taille suffisante.
- Concernant les breakpoints, nous avons convenu avec le client
d’utiliser 992 px et 768 px.
992 px pour les écrans d’ordinateurs et 768 px pour les tablettes, et
tout ce qui est en dessous de 768 pour les téléphones portables.
- Il faut d’abord réaliser l’intégration pour les ordinateurs (autrement
dit, en desktop first), puis les tablettes et enfin les téléphones.
L’utilisation des Media Queries nous permettra de réaliser
l’intégration pour les différents supports.
- Plusieurs formats et tailles d’images ont été exportés. Il faudra choisir
le format le plus adapté par rapport à la résolution et au temps de
chargement. **OK mais justifier dans la présentation**
- Les icônes proviennent de la bibliothèque Font Awesome. Nous
pouvons passer par un CDN pour faciliter le chargement des icônes.
- Les couleurs de la charte sont le bleu (#0065FC), une version plus
claire de ce bleu (#DEEBFF) et le gris pour le fond (#F2F2F2). **OK**
- La police du site est Raleway. Nous pouvons passer par Google Font
pour importer facilement cette police dans le code :
https://fonts.google.com/specimen/Raleway. **OK**
- Il est important d’utiliser les pixels et les pourcentages plutôt que les
REM et les EM. Le client préfère cette solution pour des contraintes
techniques. **OK**
- Il est important d’utiliser Flexbox plutôt que Grid. Notre client est
plus à l’aise avec cette solution. **OK**
- Aucun framework CSS (type BootStrap ou Tailwind CSS) ou
préprocesseur CSS (type Sass ou Less) ne doit être utilisé. **OK**
- Il est important d’utiliser des balises sémantiques (type `main`,
`header`, `nav`, etc.). **OK**
- Le code doit être valide aux validateurs W3C HTML et CSS. **TO DO**
- La maquette doit être compatible avec les dernières versions de
Google Chrome et de Mozilla Firefox. Il faudra tester le prototype sur
ces deux navigateurs. **TO DO**
- Le code ne doit pas être versionné avec Git.
___

## <a id="j1"> Jour 1</a>

### HTML

- `<meta charset="UTF-8">` -> ?
- `<meta http-equiv="X-UA-Compatible" content="IE=edge">` -> ?
- Noms des `id` et `class` HTML assez longs > chercher si il y a des bonnes pratiques

### CSS

J'ai essayé d'appliquer un style (`background-color`) à un  `<nav>`. Ca n'a pas fonctionné.  
En revanche ça fonctionne sur le div que j'ai rajouté à l'intérieur.  
Certains éléments HTML ne sont probablement pas censés être mis en forme car non affichés. A vérifier.

### GIT / GITHUB

- GITHUB : Comprendre pourquoi la commande *push* fonctionne dans VS Code mais pas dans Github Desktop dans mon projet

### DIVERS

- Regarder des exemples de README.MD pour savoir quoi mettre dedans
- Me renseigner sur les licences

### NOUVEAUTES
- Emmet dans VS Code (https://code.visualstudio.com/docs/editor/emmet)  
`! + Entrée` pour pré-remplir la page HTML avec le doctype HTML, un head, des métadonnées  
`<! + Entrée` pour pré-remplir la page HTML avec le doctype HTML  
`.classname` pour créer un div avec *classname* comme nom de classe  
`#idname` pour créer un div avec *idname* comme id  
`ul>li*x` pour créer une liste non ordonnée avec *x* éléments dedans / testé avec des divs avec une classe commune. Super pratique pour les éléments dans ma galerie.

- Github CLI installé (https://cli.github.com/manual/index)

## <a id="j2">Jour 2</a>

### HTML

- ` <meta charset="UTF-8">`

> **`<meta>`**  
L'élément HTML `<meta>` représente toute information de métadonnées qui ne peut pas être représentée par un des éléments (`<base>`, `<link>`, `<script>`, `<style>` ou `<title>`)  
https://developer.mozilla.org/fr/docs/Web/HTML/Element/meta


> ***charset***  
> Cet attribut déclare l'encodage utilisé par la page.  
[...]  
Les auteurs sont invités à utiliser UTF-8.  
https://developer.mozilla.org/fr/docs/Web/HTML/Element/meta

> The charset attribute specifies the character encoding for the HTML document.  
The HTML5 specification encourages web developers to use the UTF-8 character set, which covers almost all of the characters and symbols in the world!  
https://www.w3schools.com/tags/att_meta_charset.asp

- **UTF-8**

> *Universal Character Set Transformation Format1 - 8 bits*
est un codage de caractères informatiques conçu pour coder l’ensemble des caractères du « répertoire universel de caractères codés », initialement développé par l’ISO dans la norme internationale ISO/CEI 10646, aujourd’hui totalement compatible avec le standard Unicode, en restant compatible avec la norme ASCII limitée à l’anglais de base, mais très largement répandue depuis des décennies.  
L’UTF-8 est utilisé par près de 95,2 % des sites web en octobre 2020.

Quelques charsets :

- ASCII
- ISO-8859-1
- ISO-8859-15
- Latin-1
- Unicode : UTF-8, UTF-16, UTF-32
- BOM
- ...

- **Liens utiles**
> https://www.w3.org/International/getting-started/characters  
> https://fr.wikipedia.org/wiki/UTF-16  
http://www.steves-internet-guide.com/guide-data-character-encoding  

___

- `<meta http-equiv="">`

>The http-equiv attribute provides an HTTP header for the information/value of the content attribute. <br>
The http-equiv attribute can be used to simulate an HTTP response header.

- `"X-UA-Compatible" content="IE=edge"`
> Permet la compatibilité avec certaines versions d'IE.
Apparemment c'est un parti-pris, car ça sous entend devoir maintenir son site pour être compatible avec des versions futures.

https://www.w3schools.com/tags/att_meta_http_equiv.asp  
https://docs.microsoft.com/en-us/openspecs/ie_standards/ms-iedoco/380e2488-f5eb-4457-a07a-0cb1b6e4b4b5  
https://n.survol.fr/n/x-ua-compatible-ieedge

- [ ] Chercher ce que sont les *quirks* (IE)

___
**HTML**

- **`<nav>`**

> L'élément HTML `<nav>` représente une section d'une page ayant des liens vers d'autres pages ou des fragments de cette page. Autrement dit, c'est une section destinée à la navigation dans un document (avec des menus, des tables des matières, des index, etc.).  
Cet élément ne possède que les attributs universels.  
https://developer.mozilla.org/fr/docs/Web/HTML/Element/nav

- **Attributs universels**

https://developer.mozilla.org/fr/docs/Web/HTML/Global_attributes
> Les attributs universels sont des attributs communs à l'ensemble des éléments HTML. Ces attributs peuvent donc être ajoutés sur tous les éléments (dans certains cas, les attributs n'auront aucun effet).  
Les attributs universels peuvent être définis sur tous les éléments HTML, y compris pour les éléments non définis dans le standard. Autrement dit, les éléments non-standards doivent pouvoir accepter ces attributs. Cela permettra au navigateur de les gérer selon certains des aspects de la spécification. Par exemple, pour un navigateur conforme, un élément ``<toto hidden>...</toto>`` sera masqué bien que ``<toto>`` ne soit pas un élément HTML valide.

> Question trouvée sur stackoverflow:  
*Why won't my nav element go to the center or change style?*  
https://stackoverflow.com/questions/19218262/why-wont-my-nav-element-go-to-the-center-or-change-style

Apparemment, pas de problème pour appliquer un style à un nav. -> Erreur de syntaxe ?

**Solution** : J'avais écrit ``#nav``, or je voulais appliquer le style à l'élément nav, pas à un élément dont l'``id="nav"``  
Ca fonctionne avec
:

```css
nav {
    color: red;
    }
```

Si on peut appliquer un style à n'importe quel élément HTML, est-ce qu'on peut mettre un style à une balise ``<head>`` ou ``<meta>`` même si ça ne se voit pas ?

### CSS

[Guide Flexbox hyper bien fait](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

A priori ça fonctionne comme la répartition des éléments dans Photoshop ou PowerPoint mais en mieux (haut, bas, gauche, droite, centré, répartir équitablement, étirer, compresser, remplir, trier, ... )  

**Problème 1**  
: j'ai l'impression que d'avoir ajouté ``display: flex`` à mon élément ``nav`` l'a fait rétrécir.  
``width: 100%`` ne change rien mais ``width: 100px`` réduit encore la taille du menu.  
``width: 1000px`` ne l'augmente pas plus que ``width: 100%``  

**Solution**
: Après inspection de la page dans Firefox, j'avais créé un ``<div id="menu">`` dans le ``<nav>``, pensant qu'on ne pouvait pas appliquer de style directement au ``<nav>``.
En réalité, mon nav n'a jamais changé de taille, mais le div avec le background jaune si.
-> Suppression du div inutile.

**Idée 1**
: Mettre mes 2 liens du menu (nav) dans un div et ajouter un ``justify-content: space-between`` entre le logo et le div des boutons pour les placer chacun à une extrémité du menu.  
-> Fait. ``<div id="navlinks">``

**Idée 2**
: j'ai l'impression que beaucoup d'éléments de ma page sont des flex containers. Avec les classes que j'ai créé je vais devoir répéter souvent ``display: flex``.  
Note pour la fin du projet : voir si je peux faire des classes plus génériques pour éviter d'avoir une feuille CSS trop longue.

Grafikart | [Tutoriel CSS : px, em et rem](https://www.youtube.com/watch?v=ZV6N6w5bMDU)  
> *px* : valeur absolue  
*em* : valeur relative par rapport à l'élément parent  
*rem* (root em) : valeur relative par rapport à l'élément racine

***em*** :
> “An em is a CSS unit that measures the size of a font, from the top of a font’s cap height to
the bottom of its lowest descender. Originally, the em was equal to the width of the capital
letter M, which is where its name originated.”   - The Principles of Beautiful Web Design  

Also found : **e**phe**m**eral unit

Kevin Powell | [Are you using the right CSS units?](https://www.youtube.com/watch?v=N5wpD9Ov_To)<br>
Kevin Powell | [em vs rem](https://www.youtube.com/watch?v=_-aDOAMmDHI)

> - Am I setting a font size? -> go with *rem* which are relative (to the font size of the root element) units like *em*  
By default the font size is 16px  
*rem* adapts to the user system and browser preferences.  
If I'm using pixels (absolute) then I may override these preferences. (not good)  
i.e. : user changed his default font size to a bigger one, and I force a smaller one, it's not super user friendly.
> - Am I setting a width?
-> a *%* coupled with ``max-width`` should work best, or ``viewport-width``  
-> or *ch* unit (1 ch = approximatively the width of the number 0).
i.e : for setting a max-width on a paragraph, I could make use of *ch* because in typography we usually go for max 75 characters per line for readability.
> - Am I setting a ***height***? -> Do I really need to set a ***height***? Can I go for a ***min-height*** instead? So if the window is shrunk it won't overflow.  
-> %, em, rem or vw can do the job.  
Attention à ``viewport-height`` qui peut poser des problèmes sur terminaux mobiles (ex quand le clavier apparaît)
>- Am I setting a margin or padding? -> em or rem  
em: relative to parent so if the parent font-size increases, margin/padding will increase too.  
rem: relative to root, so if the parent font-size increases, margin/padding won't change.
 
> Note on media queries : em recommended for consistency across browsers because Safari processes rem and pixels differently than other browsers.  
[Zell's article on media queries](https://zellwk.com/blog/media-query-units/)

Conclusion : units I should focus on: %, em, rem, a bit of ch and viewport


Liens utiles
> https://stackoverflow.com/questions/7678883/is-it-better-to-define-images-in-direct-html-or-css  
> [5 CSS mistakes that I see way too often](https://www.youtube.com/watch?v=iHEkRIF7zxI)  
> [5 mins about Media Queries](https://www.youtube.com/watch?v=2KL-z9A56SQ)  
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

- La border-top sur les liens du menu décale le bouton vers le bas.  
Solutions possible : mettre une bordure invisible/blanche sur les ``a:link, a:visited`` ou trouver un moyen de placer la bordure à l'intérieur
- J'ai importé tous les styles de Raleway, ne pas oublier d'enlever ceux qui sont inutiles.
- La hauteur du header et du logo sont complètement arbitraires
- Balises ``article`` et ``picture`` découvertes. Documentation à lire sur le sujet. Article est une balise sémantique, probablement mieux qu'un div pour mes tuiles. Picture est a priori mieux que img car plus d'options pour les sites responsives (voir lesquelles et si utile dans le projet).

- Visuellement on dirait que le div "Les plus populaires" est un enfant de "Hébergements à Marseille" (background rouge), or ils sont enfants du même parent. Revoir la hiérarchie, et retravailler les flexbox.

## <a id="j3"> Jour 3</a>

Flexbox :

**display: inline-flex**

> If we didn’t want div elements to be block-level elements, we would use display: ``inline``. Flexbox, however, provides the ``inline-flex`` value for the display property, which allows us to create flex containers that **are also inline elements**.\
[Codecademy - Learn intermediate CSS](https://www.codecademy.com/courses/learn-intermediate-css/)  

> In HTML programming, a block-level element is any element that starts a new line (e.g., paragraph) and uses the full width of the page or container. A block-level element can take up one line or multiple lines and has a line break before and after the element.
https://www.computerhope.com/jargon/b/block-level-element.htm  

> ``display: inline-flex`` does not make flex items display inline. It makes **the flex container display inline**. That is the only difference between ``display: inline-flex`` and ``display: flex``. A similar comparison can be made between display: ``inline-block`` and ``display: block``, and pretty much any other display type that has an inline counterpart.\
\
**There is absolutely no difference in the effect on flex items**; flex layout is identical whether the flex container is block-level or inline-level. In particular, the flex items themselves always behave like block-level boxes (although they do have some properties of inline-blocks). You cannot display flex items inline; otherwise you don't actually have a flex layout.\
It is not clear what exactly you mean by "vertically align" or why exactly you want to display the contents inline, but I suspect that flexbox is not the right tool for whatever you are trying to accomplish. Chances are what you're looking for is just plain old inline layout (display: inline and/or display: inline-block), for which flexbox is not a replacement; flexbox is not the universal layout solution that everyone claims it is (I'm stating this because the misconception is probably why you're considering flexbox in the first place). \
\
[Q&A stackoverflow](https://stackoverflow.com/questions/27418104/whats-the-difference-between-displayinline-flex-and-displayflex)  
> When we add display: flex, we are really defining display: **block** flex.  
https://www.smashingmagazine.com/2018/08/flexbox-display-flex-container/
MERCI !!!!

https://discuss.codecademy.com/t/whats-the-difference-between-display-flex-and-display-inline-flex/370020

https://css-tricks.com/multiple-class-id-selectors/

## <a id="j4">Jour 4</a>

### CSS cool stuff

"Text is always king"

`::before` and `::after` pseudo elements  
https://www.youtube.com/watch?v=zGiirUiWslI  
https://www.youtube.com/watch?v=xoRbkm8XgfQ  
https://www.youtube.com/watch?v=QFjqxVMwIl8  

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
- `gradient`, `linear`, `radial`,`conic`, `repeating`,..., 

https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/radial-gradient()

[How to create a duotone effect and mix blend modes](https://egghead.io/lessons/css-use-css-pseudo-elements-and-mix-blend-mode-to-create-a-duotone-style-effect)

Box shadow:  
- https://www.youtube.com/watch?v=u6Rur7G8HNY
- https://tobiasahlin.com/blog/how-to-animate-box-shadow/
- https://codepen.io/kevinpowell/pres/abmOeoG

A mettre dans ma page !!!
En bref : on crée un calque avec l'ombre déjà présente, et on la toggle avec ``transition: opacity 1s ease;``  
Cas 1 : on crée une box-shadow
Différence : l'ombre est déjà calculée, on change juste son opacité  
Différence dans l'exemple : 32ms rendering + 18ms painting contre 20ms rendering + 2ms painting  

Emmet : go to matching pair (pratique pour mon wrapper)

___
> **Padding as a void** In the initial CSS implementation by Netscape Navigator 4, padding was sometimes a void.  What I mean is, you could give an element a background color, and you could set a border, but if you adding any padding, in some situations it wouldn’t take on the background color, allowing the background of the parent element to show through.  Today, we can recreate that effect like so: 

```css
    border: 3px solid red;
    padding: 0.5em;
    background-color: cornflowerblue;
    background-clip: content-box;
```

https://meyerweb.com/
___

### Markdown

Trouver un système de catégories en markdown/html pour récupérer tous les éléments correspondant et les exporter vers un autre markdown (ex : "CSS_stuff.md", "Emmet_shorhands.md")  
Possibilité d'utiliser une classe HTML dans le markdown mais besoin d'un script pour extraire les paragraphes correspondants et les écrire dans les autres markdowns.  
-> a voir quand j'aurai appris javascript/node.js

___

### CSS 

Explication et exemples d'imbrication de propriétés CSS (nesting)  
https://www.pierre-giraud.com/html-css-apprendre-coder-cours/imbrication-heritage-etendu/  

### Parenthèse "UI/UX après visite du site de Pierre Giraud"

 La croix pour fermer la pop-up qui s'affiche sur sa page est située **en bas à gauche** de la pop-up.  
D'ordinaire elle soit situé en haut à droite dans les fenêtres Windows, en haut à gauche sur Linux et Mac.  

**Question naïve :** est-ce qu'il y a des études menées en ergonomie sur les mouvement du bras lorsqu'on déplace la souris ?  
Observation perso : faire un mouvement d'adduction de l'épaule a l'air de demander moins d'effort que de faire un mouvement d'adbduction, et le mouvement me semble plus précis.  
(Le problème se pose moins dans le cas d'une fenêtre en plein écran car la souris arrive en butée en haut à droite de l'écran.)

Pourquoi les boutons de contrôle d'une fenêtre sont situés en haut et pas en bas, alors qu'ergonomiquement ça semble plus confortable d'y accéder quand ils sont en bas.

-> Peut être parce qu'en bas il y a le menu démarrer ou le dock et que ça évite de cliquer accidentellement dessus.  
-> Ou peut être pour dissuader de fermer la page/ pop-up. :joy:  
-> Ou c'est une question de sens de lecture, et qu'on considère que les contrôles (Ficher, Edition,... [x] Fermer la page) précèdent le contenu.

Liens connexes: https://ux.stackexchange.com/questions/23733/what-is-better-window-buttons-on-the-left-os-x-or-on-the-right-windows

> **I think this is one of those things where you should do what the user expects.**
> What do they expect? Well that's sometimes the tricky thing to figure out. Eye movement studies have been done in excess to determine the best placement for the most important call-to-action buttons. And users often start in the upper-left hand corner. On the other hand, these window buttons are so ubiquitous and so familiar that they shouldn't require unnecessary thought. If a user is accustomed to an OS with the buttons on a certain side of the screen they will naturally be looking for them in that spot. Past experience is going to be the dominant factor in what the user expects. 
So for example, if your audience is composed of 90% Windows users, I think you should absolutely put these buttons in the upper-right. Windows users will naturally look in the upper-right hand corner for these buttons because that's what they've been trained to do. 
Or better yet, if you can adopt the built-in window controls (title and button placement) of the target OS, then it takes this decision out of your hands and the buttons will always be where the user expects.
https://ux.stackexchange.com/questions/7/what-is-the-important-aspect-to-consider-when-deciding-where-windows-interaction

-> Problème de ce raisonnement, si on dispose les éléments par rapport à ce que les utilisateurs ont l'habitude de voir, on ne peut rien faire évoluer.  
Point intéressant du post : on place les éléments par rapport au regard/sens de lecture (début : haut/gauche) / lecture en Z,...
donc "ergonomie" pas au sens anatomique (mouvement d'épaule, du bras, de la main).  
Pistes à explorer
:
- Les mouvements de curseur des joueurs de FPS. (ex: Razer et son app de heatmaps et de tracking de curseur) 
- Des études d'ergonomie sur le placement des éléments fréquemments utilisés, dans une page web ou une app.

___

## CSS 

NESTING
https://www.alsacreations.com/tuto/lire/545-Comprendre-l-heritage-et-la-parente-des-styles-CSS.html

Il y a un héritage "natif" concernant les balises ``<a>`` et ses enfant (pseudo classes ``:link`` ``:visited``, ``:hover``, ``:active``)

```css
    .menu li {
        propriétés
    }
```

éléments li dont le parent à la classe "menu"

```css
    li .menu {
        propriétés
    }
```

éléments de la classe menu dont le parent est un ``<li>``

```css
    li, .menu {
        propriétés
    }
```

pas d'héritage ici (avec la virgule), c'est juste pour grouper les propriétés d'éléments sans rapport, comme dans mon CSS :

```css
    html, body {
        width: 100%;
    }
```

```css
    li.menu {
        propriétés
    }
```

Elément `<li>` qui possède la classe ``menu``

Aucune explication sur cette page du sélecteur d'imbrication `&` ni de la règle `@nest`.

[CSS Nesting Module - W3C First Public Working Draft, 31 August 2021](https://www.w3.org/TR/css-nesting-1)

```css
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
```

Nesting allows the grouping of related style rules, like this:

```css
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
```

https://stackoverflow.com/questions/4564916/nesting-css-classes

**Le nesting n'est pas encore possible en vanilla CSS. Seulement avec Sass et Less (chercher ce que c'est).**

Problème rencontré avec la section Activités à Marseille

J'ai essayé de mettre les 6 cartes dans 1 seul container flex avec comme propriétés :

```css
    flex-flow: column-wrap;
    justify-content: space-between;
```

Les 2 grandes cartes font 100% de la ``height:990px`` du container, et les plus petites cartes s'empilent bien.

Problème : l'inversion du main et du cross axis fait que si on réduit la largeur de la page, les cartes débordent.

Test 2 : j'ai rajouté 2 divs, chacun englobe 2 petites cartes.
Le container flex est maintenant en :

```css
    flex-wrap: wrap;
    justify-content: space-between;
```

les divs "colonne" en :

```css
    flex-direction: column;
    justify-content: space-between;
```

Nouveau problème : les tags ``<a>`` autour des ``<article>`` ne sont pas des éléments flex.  
J'aimerais éviter de mettre une propriété flex à des ``<a>`` car ça ne fait pas de sens.  
Mettre les ``<a>`` dans les ``article`` ne résoud pas le problème car l'``<article>`` est aussi un container flex.

```html
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
```

___
### To do

- PAGE : Revoir toutes les margin-bottom et les regrouper
- PAGE : vérifier les règles en doublons avec l'ajout de normalize.css (box-sizing,...)
- PAGE : vérifier si ma méthode d'import de FontAwesome est bonne (CDN ?)
- **OK** PAGE : créer et ajouter une favicon 

- **OK** NAV : ajouter des liens vers les sections au menu
- SECTION SEARCH FORM : mettre en forme la barre de recherche et les filtres, passer l'icone "i" en `::before` du `<p>`
- SECTION SEARCH FORM : Trouver une meilleure solution que du padding à la mano pour l'icone FA child.
- **OK** SECTION CITY RESULTS : Ajouter une ancre aux sections
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
- REPO GIT : Mettre à jour le Readme
___

## <a id="j5"> Jour 5 </a>

**Favicon**  
Choix concernant l'extension et les dimensions de la favicon :  
https://developer.mozilla.org/fr/docs/Glossary/Favicon  
https://stackoverflow.com/questions/4014823/does-a-favicon-have-to-be-32%C3%9732-or-16%C3%9716

Ca fonctionne en 32px.
Peut être ajouter une version 72px pour les écrans retina. (accessoire)

DupChecker :

```console
------------------ Results ------------------
    ⚙️[trimStart] [trimEnd] [trimChars: ^\.[\w\-\s\.>:,\[\]\*\=]+{]
    ✅28 duplicate values found in 351 lines:
    }
    font-size: 14px; CORRIGE
    display: flex; IGNORE
    align-items: center; IGNORE
    text-decoration: none; CORRIGE
    flex-direction: column; IGNORE
    padding: 10px 10px; IGNORE
    font-weight: var(--fw-bold); IGNORE
    border: none; IGNORE
    margin-bottom: var(--mgn-bottom); IGNORE
    background-color: var(--clr-light-grey); IGNORE
    color: var(--clr-blue); IGNORE
    border-radius: 100%; CORRIGE -> 50% au lieu de 100% après test de l'exemple stackoverflow
    justify-content: space-between; IGNORE
    width: 100%; IGNORE
    border-radius: 15px; IGNORE
    color:var(--clr-blue); IGNORE
    padding: 16px; IGNORE
    align-self: flex-start; IGNORE
    background-color: white;
    font-size: var(--fs--small);
    box-shadow: var(--box-shadow);
    object-fit: cover;
    border-top-left-radius: 15px;
    flex-flow: row wrap;
    height: 495px;
    height: 100%;
    border-top-right-radius: 15px;
```

https://stackoverflow.com/questions/55410657/what-is-the-difference-between-border-radius-50-and-100

J'ai réussi à implémenter un effet sur les cartes, en suivant l'exemple de
https://tobiasahlin.com/blog/how-to-animate-box-shadow/

En revanche, j'ai été confronté à un problème spécifique à ma page, car mes cartes ont une bordure de 5px arrondie, et l'ombre du calque invisible (`.pseudo-hover::after`) est au dessus de la bordure.

J'ai tenté de résoudre le problème en ajoutant la même bordure au `.pseudo-hover::after` mais ça n'a pas marché.

J'ai inversé la marge (`margin: -5px;`) et ça fonctionne.

> Si la propriété est différente de none, un contexte d'empilement sera créé. Dans ce cas, l'élément agira comme le bloc englobant pour les éléments qu'il contient et qui ont position: fixed; ou position: absolute;.

https://developer.mozilla.org/fr/docs/Web/CSS/transform
https://www.w3.org/TR/CSS2/visudet.html#abs-non-replaced-height
https://stackoverflow.com/questions/11495200/how-do-negative-margins-in-css-work-and-why-is-margin-top-5-margin-bottom5
https://www.w3.org/TR/CSS2/visudet.html#abs-non-replaced-height

Problème posé par cette solution : le pseudo élément `::after` est au dessus du lien.

> Pseudo-elements are treated as descendants of their associated element. To position a pseudo-element below its parent, you have to create a new stacking context to change the default stacking order.
Positioning the pseudo-element (absolute) and assigning a z-index value other than “auto” creates the new stacking context.

https://developer.mozilla.org/fr/docs/Web/CSS/z-index
https://stackoverflow.com/questions/3032856/is-it-possible-to-set-the-stacking-order-of-pseudo-elements-below-their-parent-e
https://stackoverflow.com/questions/2503705/how-to-get-a-child-element-to-show-behind-lower-z-index-than-its-parent
https://stackoverflow.com/questions/54897916/why-cant-an-element-with-a-z-index-value-cover-its-child
https://stackoverflow.com/questions/3839178/how-to-use-z-index-within-an-a-tag

```css
Solution fonctionnelle : 
    a {
    position: relative;
    z-index: 5;
    }
```

Comment savoir combien de niveaux maximum de z-index j'ai dans ma page, pour éviter de mettre `z-index: 2147483647;`
https://stackoverflow.com/questions/491052/minimum-and-maximum-value-of-z-index

https://www.digitalocean.com/community/tutorials/css-z-index

Given two HTML elements, the deeply nested HTML element will always get overlapped by a less-nested HTML element with a lower z-index value.

```html
    <div class="blue">
        <div class="violet"></div>
        <div class="purple"></div>
    </div>
    <div class="green"></div>
```

```css
    .blue {
    position: relative;
    z-index: 2;
    background-color: blue;
    }
    .violet {
    position: relative;
    z-index: 4;
    background-color: violet;
    }
    .purple {
    position: relative;
    z-index: 1;
    background-color: purple;
    }
    .green {
    position: relative;
    z-index: 3;
    background-color: green;
    top: -4em;
    }
```

The HTML element div.violet will get overlapped by div.green despite having a higher z-index value!

> In CSS code bases, you’ll often see z-index values of 999, 9999 or 99999. This is a perhaps lazy way to ensure that the element is always on top. It can lead to problems down the road when multiple elements need to be on top. Most of the time you’ll find that a z-index of 1 or 2 will suffice for your needs. 

Sauf qu'il s'agit d'un cas particulier car
```html
    <a href="#">
        <article class="card pseudo-hover">
            Contenu de la carte
        </article>
    </a>
```
avec

```css
.pseudo-hover {
    position: relative;
}

.pseudo-hover::after {
    content:'';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    opacity: 0;
    border-radius: 15px;
    margin: -5px;
    box-shadow: var(--box-shadow-hover); 
}

.pseudo-hover:hover::after {
    opacity: 1;
    transition: opacity .25s ease;
} 
```

Le pseudo élément ``::after`` crée un nouveau contexte d'empilement par avec son parent . <br>
> Within a stacking context, child elements are stacked according to the same rules previously explained. Importantly, the z-index values of its child stacking contexts only have meaning in this parent. Stacking contexts are treated atomically as a single unit in the parent stacking context.

https://www.oreilly.com/library/view/developing-web-components/9781491905685/ch04.html

or `<a>` n'est pas son parent.

Solution :

```css
    a {
        position: relative;
        z-index: 3; /* (soit > à tous les autres éléments du stacking context "général") */
    }
```

De cette manière, `<a>` repasse au dessus de `<article>` et de son pseudo élément `::after`

[Documentation z-index - MDN ](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context)

> In summary
: Stacking contexts can be contained in other stacking contexts, and together create a hierarchy of stacking contexts.  
Each stacking context is completely independent of its siblings: only descendant elements are considered when stacking is processed.  
Each stacking context is self-contained: after the element's contents are stacked, the whole element is considered in the stacking order of the parent stacking context.  

[Q/A Card margins and padding - StackOverflow](https://stackoverflow.com/questions/38078957/can-we-define-min-margin-and-max-margin-max-padding-and-min-padding-in-css)

___

### To do

- [ ] PAGE : vérifier si ma méthode d'import de FontAwesome est bonne (CDN ?)
- [ ] SECTION ACTIVITIES RESULT : Le wrap des 2 cartes d'un coup parce qu'elles sont dans la même colonne est très moche. -> sera réglé par les media queries
- [ ] REPO GIT : Mettre à jour le Readme
- [x] Les ombres au hover sont plus marquées dans la partie Hébergements à Marseille que dans les autres blocs

___

[Extrait documentation sur les `<label>` - MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/Label)

> Il ne faut pas placer d'éléments interactifs (tels que les ancres (``<a>``) ou les boutons (`<button>`) dans un élément label sinon il sera difficile d'activer le contrôle associé à ce libellé.

> Placer des éléments de titres à l'intérieur d'un élément label causera des interférences avec de nombreux outils d'assistance car les titres sont généralement utilisés comme une aide à la navigation

> Un élément `<input>` avec type="button" et un attribut value valide ne nécessite pas l'ajout d'un libellé. Rajouter un libellé inutile pourra créer des interférences avec les outils d'assistance. Il en va de même pour l'élément `<button>`.

On peut également créer un lien implicite en imbriquant l'élément `<input>` directement au sein d'un élément `<label>` . Dans ce cas, les attributs for et id ne sont plus nécessaires.

```html
    <label>Aimez-vous les petits pois ?
        <input type="checkbox" name="petits_pois">
    </label>
```

[Container query instead of media queries - YouTube](https://www.youtube.com/watch?v=fuiEYR6Hoe0)

Est-ce que max-width est inclusif ? : Oui.
[Q/A - StackOverflow](https://stackoverflow.com/questions/13241531/what-are-the-rules-for-css-media-query-overlap)

___

## <a id="j6"> Jour 6 </a>

To do:

- [x] Section Hébergements à Marseille : comprendre comment flex-grow et flex-shrink se comportent pour remplacer le flex-basis. Faire des tests à côté
- [x] Section Filtres : faire une animation sur les filtres (simple et performante).  
- [x] Vérifier si des changements de layout sont nécessaires avec un breakpoint à 768px
- [ ] Faire le style pour les mobiles

- [x] Mettre les icones des filtres dans des divs : pour éviter le padding individuel en pixel des icones... mieux : mettre les icones en ::before

- J'utilise gap pour des containers flex : non supporté par Safari
Safari ne supporte gap que pour les grid.

[Article sur les % CSS - James Fisher](https://jameshfisher.com/2019/12/29/what-are-css-percentages/) <br>
[Article sur le calcul des border radius en CSS - StackOverflow](https://stackoverflow.com/questions/29966499/border-radius-in-percentage-and-pixels-px-or-em)

## <a id="j7"> Jour 7 </a>

To do
:

- [ ] Rework boutons header
- [ ] Rework @mobile boutons header
- [ ] Ajouter l'icone de loupe
- [ ] Terminer media queries mobile
- [ ] Fix le layout de la section Activités

## <a id="j8"> Jour 8 </a>

Je veux améliorer la section "Hébergements à Marseille"
Je crois que tous les éléments HTML ne se comportent pas de la même façon quand ce sont des containers ou des éléments flex.

Pas de travail direct sur le projet aujourd'hui, je vais me consacrer à faire des tests sur une page à part avec tous les éléments que je connais.


## <a id="j8"> Jour 9 </a>

Objectif : terminer la page.

To do :

Réparer cette erreur :
L’ancrage de défilement a été désactivé dans un conteneur de défilement en raison de trop nombreux ajustements consécutifs (10) avec une distance totale trop petite (0.195000004768372 px en moyenne, 1.95 px au total).
[Guide : ancrage du défilement (scroll anchoring)](https://developer.mozilla.org/fr/docs/Web/CSS/overflow-anchor/Guide_to_scroll_anchoring)

- [x] Rework boutons header
- [x] Rework @mobile boutons header
- [x] Terminer la réparation du bloc Hébergements à Marseille
- [x] Terminer les media queries mobile et tablette
- [x] Importer l'icône de loupe et lui faire remplacer le texte rechercher en version mobile (attention au border radius)
- [x] Remettre classe pseudo hover sur toutes les cartes
- [x] icones boutons à diamètre fixe en pixel
- [x] Vérifier que le fix pour l'espacement entre les lignes des détails de carte fonctionne dans tous les cas
- [x] Vérifier la présence d'éventuelles règles en doublon dans le CSS (penser à regarder normalize.css aussi)
- [ ] Préparer un support de présentation : Recontextualisation du projet, présentation du livrable, effets/ancres, 5 minutes max sur le code avec accent sur les aspects complexes

Changements décidés pour terminer le projet :

- Les liens du menu dans une ul, j'opte pour un div parce que plus simple pour utiliser flex-grow
- La section Activités à Marseille en `flex-direction: column` dans la version desktop, finalement faite en row, avec 2 divs supplémentaires pour contenir les petites cartes.