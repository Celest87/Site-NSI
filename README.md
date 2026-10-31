# Projet NSI : l'impact de l'IA sur les métiers de l'informatique

## Présentation du projet

Ce site présente quelques effets de l'intelligence artificielle sur les métiers de l'informatique. Il est composé de deux pages HTML qui partagent la même feuille de style, `contenu.css`.

## Texte pour l'oral (environ 10 minutes)

### Introduction

Bonjour, je vais vous présenter mon site réalisé en HTML, CSS et JavaScript. Le sujet est l'impact de l'intelligence artificielle sur les métiers de l'informatique.

J'ai choisi ce sujet parce que l'IA est de plus en plus présente dans les outils numériques. Elle peut aider à écrire du code, à analyser des informations ou à automatiser certaines tâches. Mais elle soulève aussi des questions : certains métiers vont-ils évoluer ou disparaître ? De quelles ressources matérielles l'IA a-t-elle besoin ? Mon site présente ces avantages et ces limites de façon simple.

Le projet comprend deux pages. La première, `index.html`, introduit le sujet et propose des éléments interactifs. La deuxième, `contenu1.html`, développe les points positifs et négatifs et les compare dans un tableau. Les deux pages utilisent `contenu.css`, ce qui permet de conserver la même apparence générale.

### Organisation des fichiers et structure HTML

Je commence par expliquer les fichiers. Un fichier HTML contient le contenu et organise les éléments de la page. Le fichier CSS définit leur apparence. Les images sont des fichiers séparés, que le HTML charge grâce à leur nom, par exemple `image.jpg` ou `OIP2.png`.

Dans `index.html`, la déclaration `<!DOCTYPE html>` indique au navigateur qu'il s'agit d'un document HTML moderne. La balise `<html lang="fr">` indique que le contenu est en français. Dans `<head>`, on trouve les informations qui ne sont pas directement affichées comme le contenu principal : l'encodage des caractères, le titre de l'onglet et le lien vers la feuille CSS. La balise `meta viewport` aide le navigateur à adapter la largeur de la page aux téléphones.

Le contenu visible est placé dans `<body>`. Les titres sont écrits avec des balises comme `<h1>` et `<h2>`, les paragraphes avec `<p>`, et la liste avec `<ul>` et `<li>`. Une image est insérée avec `<img>`. Son attribut `alt` donne une description textuelle, utile si l'image ne s'affiche pas ou pour les outils d'accessibilité.

La page utilise également des liens. Le lien vers `contenu1.html` ouvre la seconde page, et l'image principale est elle-même cliquable pour y accéder. Le lien `href="#details"` est une ancre interne : il fait défiler la page jusqu'à l'élément dont l'identifiant est `details`. Un `id` identifie un élément précis, alors qu'une `class`, comme `mini-section`, peut être réutilisée sur plusieurs éléments. Le lien « Sources des informations » mène directement à la section des références de la deuxième page.

### Contenu de la première page

La première page commence par présenter le sujet et l'illustrer avec une image. Une liste résume des changements liés à l'IA : automatisation des tâches, analyse rapide des données et évolution des compétences. Deux encadrés distinguent ensuite des avantages et des inconvénients.

La page donne aussi une définition du terme « IA ». La définition est placée dans un élément HTML à l'intérieur du mot. Dans le CSS, le sélecteur `:hover` permet de la montrer lorsque la souris passe au-dessus du mot. C'est un exemple d'interaction réalisée sans JavaScript.

Le schéma numéroté détaille quatre étapes : collecte de données, entraînement d'un modèle, production d'un résultat, puis évaluation et amélioration. Il donne matière à expliquer le fonctionnement général pendant l'oral, sans prétendre décrire toutes les méthodes d'intelligence artificielle.

La page contient également un bloc météo fixe : il sert d'exemple et n'est pas mis à jour en direct. Le schéma y détaille quatre étapes — collecte des données, entraînement, résultat, puis évaluation — pour fournir des éléments à expliquer pendant l'oral. La vidéo a été déplacée sur la deuxième page pour garder une première page plus légère.

### Deuxième page et navigation

Dans `contenu1.html`, je développe les avantages et les risques dans des paragraphes plus courts. Ils parlent du gain de temps, de l'aide à l'analyse, de l'évolution possible des emplois, de la nécessité de vérifier les résultats et des besoins en matériel et en énergie.

L'icône en forme de maison est une image cliquable. Elle est placée dans un lien vers `index.html` : en cliquant dessus, on revient à l'accueil. Son identifiant `maison` permet au CSS de la réduire et de la placer dans un coin de la page.

Le tableau compare les points positifs et les points de vigilance. Les balises `<th>` servent aux en-têtes centrés des colonnes et les balises `<td>` aux cellules contenant les informations. La vidéo et la conclusion enrichie se trouvent aussi sur cette deuxième page, suivies de sources et d'une note transparente sur l'utilisation d'une IA comme aide à la rédaction et au code.

### La feuille de style CSS

Le fichier `contenu.css` est partagé par les deux pages grâce à la balise `<link>`. Ainsi, une même règle peut styliser tous les titres, images, liens ou boutons du site.

La règle `body` définit la police, la largeur maximale, les marges, l'espacement des lignes et les couleurs principales. Le fond est composé de plusieurs dégradés superposés : les formes radiales créent des halos colorés et le dégradé linéaire donne une base sombre. La règle `@keyframes` décrit les différentes positions de l'arrière-plan, et `animation` fait évoluer ces positions pendant 18 secondes, en boucle. Cela crée l'effet de fond animé sur le thème de l'IA.

Les sélecteurs CSS peuvent viser une balise, une classe ou un identifiant. Par exemple, `h1` concerne les grands titres, `.mini-section` concerne les blocs qui partagent cette classe, et `#maison` ne concerne que l'image portant cet identifiant. Le point désigne une classe et le dièse un identifiant.

Le CSS améliore aussi la lisibilité : les blocs ont des marges, du remplissage intérieur, une bordure et des coins arrondis. L'image principale possède une classe dédiée pour limiter sa largeur et sa hauteur, sans modifier l'icône de retour. La liste numérotée du schéma est espacée pour faciliter sa lecture à l'oral. Les boutons changent de couleur au survol grâce à `button:hover`. Le tableau utilise `border-collapse` pour rapprocher ses bordures et former une grille visuelle ; les titres de colonnes sont centrés. Une règle `@media` adapte la grille et la taille du tableau aux petits écrans.

Les règles `.cache` et `.cache.visible` contrôlent l'affichage de la réponse à la devinette. Par défaut, `display: none` la masque. Quand la classe `visible` est ajoutée, `display: block` la rend visible. La définition du mot utilise un principe comparable : elle est cachée par défaut, puis affichée avec `.term:hover .def` lorsque le pointeur survole le terme.

### JavaScript et interactions

À la fin de `index.html`, le JavaScript ajoute les interactions. La variable `clics` commence à zéro. Un écouteur d'événement est associé au bouton : à chaque clic, le compteur augmente et le texte de la page est actualisé.

Pour compter les visites, le programme utilise `localStorage`. C'est une petite mémoire du navigateur qui conserve une valeur même après fermeture de la page. Le programme lit l'ancienne valeur, la convertit en nombre, ajoute une visite, puis enregistre et affiche le nouveau total. Ce compteur est limité au navigateur et à l'appareil utilisés : ce n'est pas un compteur centralisé qui additionne les visites de tous les visiteurs.

Le bouton « Afficher » utilise `classList.toggle('visible')`. Cette instruction ajoute la classe si elle est absente et la retire si elle est présente. Le CSS se charge alors de cacher ou d'afficher la réponse. Enfin, `setInterval` exécute une fonction toutes les 1 000 millisecondes, donc chaque seconde. La fonction augmente la variable `secondes` et met à jour le nombre visible sur la page.

### Conclusion

Pour conclure, ce site m'a permis d'utiliser plusieurs notions de NSI et de développement web : structurer une page avec HTML, appliquer un style commun avec CSS, sélectionner des éléments avec des classes et des identifiants, et rendre la page interactive avec JavaScript.

J'ai également appris à relier plusieurs pages et à utiliser des événements comme le clic et le survol. Le sujet montre que l'IA peut être un outil utile pour les informaticiens, mais qu'il faut aussi réfléchir à ses effets sur les emplois, aux compétences nécessaires et aux ressources matérielles mobilisées.

Le site reste volontairement simple : le compteur de visites dépend du navigateur, les données météo sont statiques et la vidéo dépend d'un service externe. Ce sont des limites que l'on pourrait améliorer dans une version plus avancée. Pour documenter les informations, la deuxième page renvoie vers des sources sur la définition de l'IA, ses effets possibles sur l'emploi et sa consommation d'énergie. Une IA a servi d'aide pour structurer et commenter le code et préparer une première version du texte ; les auteurs doivent vérifier les contenus et les sources. Merci de votre attention.

## Travail demandé dans le projet

- Une feuille CSS comprenant au moins dix propriétés et des sélecteurs de balise, classe et identifiant.
- Deux pages distinctes reliées par des liens.
- Une liste, une image cliquable, une source et un lien ancre.
- Des éléments multimédias ou visuels : schéma, vidéo et exemple météo.
- Des fonctions : compteur de visites, réponse affichée au clic et définition affichée au survol.
- Une présentation orale d'environ dix minutes.
- Un dossier final avec l'adresse du site, des captures d'écran et un diaporama.





Première page :

    - Améliorer le schéma pour nous donner du temps a l'oral
    - Mettre la conclusion sur la deuxième page
    - Rétrécir la prémière image
    - Enlever les premiers tableaux et les laisser sur la deuxieme page
    - Mettre le JavaScript tout en bas de la première page
    - Mettre une devinette
    - Voir pour déplacer la vidéo

Deuxième page :

    - Rétrécir ou enlever les grands paragraphes
    - Centre les titres des colonnes dans le tableau
    - Mettre la conclusion en bas de la page et l'enrichir
    - Rajouter les sources de nos informations et préciser si possible quand on a utilisé l'ia (en mentant, un peu, si besoin)

Aussi :

    - Rajoute plus de commentaires