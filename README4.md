# Explication détaillée du code du site

Ce document explique le fonctionnement des deux pages HTML et de leur feuille de style commune. Le site parle de l'impact de l'intelligence artificielle sur les métiers de l'informatique.

## Fichiers du projet

- `index.html` : page d'accueil, introduction, devinette et explication simplifiée du fonctionnement d'une IA.
- `contenu1.html` : deuxième page, avec les effets de l'IA, un tableau, une vidéo, les sources et les compteurs.
- `contenu.css` : apparence commune aux deux pages.
- `image.jpg` et `OIP2.png` : images utilisées sur les pages.

Les deux pages chargent `contenu.css` avec une balise `<link>`. Modifier ce fichier change donc l'apparence des deux pages.

## `index.html` : la page d'accueil

### Début du document

`<!DOCTYPE html>` indique au navigateur que le fichier utilise HTML moderne. La balise `<html lang="fr">` précise que le contenu est en français.

Dans `<head>`, les balises `<meta>` règlent l'encodage des caractères et l'affichage sur les petits écrans. La balise `<title>` donne le nom affiché dans l'onglet du navigateur. Enfin, `<link rel="stylesheet" href="contenu.css">` relie la page au CSS commun.

### Contenu de la page

- Le `<h1>` donne le titre principal.
- Le paragraphe `.intro` présente le sujet. La classe `intro` permet de centrer ce texte en CSS.
- L'image `image.jpg` est placée dans un lien vers `contenu1.html` : cliquer sur l'image ouvre la deuxième page. Son attribut `alt` décrit l'image si elle ne s'affiche pas et aide les personnes utilisant un lecteur d'écran.
- La liste `<ul class="liste">` présente trois changements liés à l'IA. Chaque élément de liste est écrit dans une balise `<li>`.
- Le lien `href="#details"` mène à l'élément qui porte `id="details"` plus bas dans la même page.
- Le bloc `.bloc` contient une question, un bouton et la réponse. La réponse porte la classe `cache`, qui la masque au départ.
- Le mot « IA » est entouré par `.term`. La définition, dans `.def`, est imbriquée dans ce mot pour que le CSS puisse la faire apparaître au survol.
- La section `#details` explique en quatre étapes un exemple simplifié du fonctionnement d'une IA. `<ol>` crée une liste numérotée.
- Les liens en bas de page donnent accès aux sources sur la deuxième page et permettent aussi de passer à celle-ci.

### JavaScript de la devinette

Le script se trouve juste avant `</body>`, après les éléments HTML qu'il utilise.

1. `document.getElementById('revelerReponse')` retrouve le bouton dans la page.
2. `onclick` dit quoi faire quand le bouton est cliqué.
3. Le script ajoute la classe `visible` au texte de la réponse.
4. Le CSS repère cette classe et affiche le texte.

La réponse reste dans le HTML, mais elle est cachée jusqu'au clic.

## `contenu1.html` : la deuxième page

### En-tête et navigation

Le début du fichier reprend les mêmes réglages HTML que la page d'accueil et charge le même `contenu.css`. L'image `OIP2.png` est placée dans un lien vers `index.html` : elle sert de bouton de retour. Son identifiant `maison` permet de régler sa taille et son emplacement en CSS.

### Parties consacrées au sujet

- Les deux premières sections `.mini-section` distinguent les points positifs de l'IA et les points de vigilance.
- Le tableau `<table>` compare ces deux aspects. Chaque `<tr>` forme une ligne, les `<th>` sont les cellules d'en-tête et les `<td>` sont les cellules ordinaires.
- La vidéo intégrée provient de la chaîne L'Étudiant et présente le métier d'ingénieur en intelligence artificielle. Le lien sous le lecteur permet de l'ouvrir directement sur YouTube si l'intégration est bloquée.
- La section `id="sources"` rassemble les références. Les liens externes utilisent `target="_blank"` pour s'ouvrir dans un nouvel onglet et `rel="noopener noreferrer"` pour limiter les risques liés à cette ouverture.
- La section « Conclusion » résume les idées principales.
- Le dernier lien de navigation ramène à `index.html`.

### Compteurs et JavaScript

Le bloc `<aside class="compteurs">` affiche les visites, les clics et le temps. Les éléments `<strong>` ont des identifiants que le script retrouve pour mettre leurs nombres à jour.

- **Visites :** `localStorage.getItem('visitesContenuIA')` lit le nombre enregistré dans ce navigateur. `Number(...)` le convertit en nombre. Si aucune valeur n'est enregistrée, `|| 0` démarre à zéro. Le script ajoute ensuite une visite et sauvegarde le nouveau total avec `localStorage.setItem(...)`. Ce total est propre au navigateur utilisé : il ne représente pas les visites de tous les internautes.
- **Clics :** la variable `clics` commence à zéro. Quand le bouton est cliqué, elle augmente de un et `textContent` affiche le nouveau total.
- **Temps :** `setInterval` répète une petite fonction toutes les 1 000 millisecondes. Elle augmente `secondes` et actualise le nombre affiché. Le temps est approximatif si le navigateur ralentit une page inactive.

## `contenu.css` : le style commun

La feuille contient **43 déclarations** et **17 propriétés CSS différentes**. Une déclaration est un réglage écrit dans une règle ; plusieurs déclarations peuvent utiliser la même propriété.

### Organisation du style

- **Fond général (`body`) :** limite la largeur, centre la page et règle l'espace intérieur, la police et la couleur du texte. Le fond combine trois halos bleu, vert et violet avec un dégradé sombre.
- **Images :** `img` empêche les images de dépasser leur conteneur. `.illustration` centre l'image principale, arrondit ses coins et ajoute une ombre bleue. `#maison` place l'icône de retour en haut à gauche.
- **Titres et sections :** `h1` centre le titre. `.liste`, `.mini-section`, `.conclusion` et `.bloc` partagent leurs marges, leur espace intérieur, un fond sombre transparent, une bordure et des coins arrondis. La conclusion utilise sa propre classe `.conclusion`.
- **Liens et bouton :** les liens sont cyan et changent de couleur au survol. Le bouton a un fond bleu, des coins arrondis et un curseur de clic ; sa couleur change aussi au survol. `transition` rend ces changements progressifs.
- **Tableau :** `table`, `th` et `td` remplissent la largeur disponible, fusionnent les bordures et distinguent visuellement les cellules d'en-tête.
- **Devinette et définition :** `.cache` et `.def` sont masqués au départ. Quand JavaScript ajoute `visible` après le clic, `.cache.visible` affiche la réponse. Le survol de `.term` affiche `.def`.

Les **17 propriétés différentes** utilisées sont `background`, `border-collapse`, `border-radius`, `color`, `cursor`, `display`, `font`, `font-weight`, `left`, `margin`, `max-width`, `padding`, `position`, `text-align`, `text-decoration`, `top` et `width`.

Les sélecteurs commençant par un point, comme `.bloc`, ciblent une classe HTML. Ceux commençant par `#`, comme `#details`, ciblent un identifiant. Les noms comme `body`, `table` ou `button` ciblent directement des balises.

## Parcours général

Depuis `index.html`, le visiteur lit l'introduction, peut cliquer sur l'image ou le lien pour ouvrir `contenu1.html`, essayer la devinette et survoler le mot « IA ». La deuxième page détaille les effets, donne les sources et affiche les compteurs. Les deux pages se relient entre elles et partagent le même fichier CSS.
