# Mini-projet NSI — L'impact de l'IA sur les métiers de l'informatique

## Présentation du site

Le site comporte deux pages HTML reliées entre elles :

- `index.html` présente le sujet, une liste, une image cliquable, une ancre, une devinette et un schéma explicatif.
- `contenu1.html` développe les avantages et les points de vigilance, avec un tableau, les sources et une conclusion.
- `contenu.css` contient la mise en forme commune aux deux pages.

Les éléments facultatifs de la fiche — météo, température, vitesse du vent, sons ou webcam — ne sont pas ajoutés. Le site ne présente ainsi aucune donnée de démonstration comme une information réelle.

## Proposition de texte pour l'oral

Bonjour, nous allons vous présenter notre mini-site réalisé pour le projet de NSI. Nous avons choisi comme sujet l'impact de l'intelligence artificielle sur les métiers de l'informatique. L'IA peut aider à écrire du code et à analyser des données, mais elle transforme aussi les tâches et les compétences attendues. Nous avons donc voulu présenter ses possibilités et les points auxquels il faut rester attentif.

Notre site est composé de deux pages HTML et d'une seule feuille de style CSS partagée. La première page, `index.html`, introduit le thème. Elle comprend une image cliquable qui conduit vers la deuxième page, une liste de changements liés à l'IA, ainsi qu'un lien ancre. Une ancre est un lien qui fait défiler la page jusqu'à un élément précis, identifié ici par `details`.

La première page contient aussi un schéma simplifié du fonctionnement d'une IA. On peut le présenter en quatre étapes. D'abord, on rassemble des données, comme des textes ou des images. Ensuite, un algorithme utilise des exemples pour entraîner un modèle et repérer des régularités. Le modèle produit ensuite un résultat lorsqu'il reçoit une nouvelle donnée ou une demande. Enfin, on évalue ce résultat et on cherche à corriger les erreurs. Ce schéma est volontairement général : les techniques exactes varient selon le type d'IA.

La deuxième page détaille les avantages et les points de vigilance. L'IA peut faire gagner du temps sur certaines tâches, aider à analyser un grand volume de données et assister les développeurs. En revanche, elle peut produire des erreurs ou reproduire des biais présents dans les données. Certaines tâches ou certains métiers peuvent évoluer. Les systèmes d'IA nécessitent aussi du matériel informatique et de l'énergie. Le tableau de la page résume ces deux aspects. Les textes restent courts pour distinguer rapidement les idées, puis le tableau les met en regard sans prétendre donner une réponse unique sur l'avenir de tous les métiers.

Nous avons utilisé HTML pour structurer le contenu. Les balises `<h1>` et `<h2>` organisent les titres, `<p>` les paragraphes, `<ul>` ou `<ol>` les listes et `<table>` le tableau. La balise `<a>` crée des liens, tandis que `<img>` affiche une image. L'attribut `alt` décrit cette image si elle ne s'affiche pas ou pour les outils d'accessibilité. Les identifiants `id` servent à cibler un élément précis, et les classes `class` permettent d'appliquer les mêmes styles à plusieurs éléments.

Le fichier `contenu.css` définit le style commun des deux pages. Le choix reste volontairement simple : fond clair, texte foncé, titres bleus, encadrés blancs et espacement régulier. Les sélecteurs comme `h1` ciblent une balise, `.mini-section` cible une classe et `#maison` cible un identifiant. Le sélecteur `:hover` affiche la définition quand le pointeur passe sur « IA ». Une règle `@media` empile les colonnes sur les petits écrans.

Pour la présentation, nous pouvons montrer d'abord les deux pages et faire les actions en direct : cliquer sur l'image pour naviguer, utiliser le lien ancre, révéler la réponse et passer la souris sur « IA ». Nous pouvons ensuite montrer les compteurs, le tableau et les sources. Ces démonstrations permettent de vérifier que le site ne contient pas seulement du texte statique.

Le JavaScript ajoute les interactions et le bloc discret en bas de la deuxième page affiche les compteurs. Le compteur de clics augmente quand on appuie sur son bouton. Le temps passé est actualisé chaque seconde grâce à `setInterval`. Les visites sont enregistrées dans `localStorage`, une mémoire du navigateur qui conserve une valeur après fermeture de la page. Ce compteur est local à un navigateur : il ne représente pas le nombre total de visiteurs du site.

Dans le code, `getElementById` récupère un élément HTML à partir de son identifiant, puis `textContent` change le nombre affiché sans reconstruire toute la page. `Number` transforme la valeur enregistrée sous forme de texte en nombre afin de pouvoir l'incrémenter. Le compteur de clics et le temps sont propres au chargement en cours, tandis que le compteur de visites est sauvegardé. Cela permet aussi de discuter d'une limite : effacer les données du navigateur réinitialise les visites enregistrées.

La devinette utilise JavaScript pour ajouter ou retirer la classe CSS `visible` quand on clique sur le bouton. La réponse est donc masquée au départ, puis affichée. La définition du mot « IA » utilise une autre méthode : elle apparaît au survol grâce au CSS.

Pour les informations, nous avons ajouté des liens vers des sources sur la définition de l'IA, l'emploi et l'énergie. Une IA a servi d'aide à la structuration et aux commentaires du code ainsi qu'à la préparation d'une première version du texte. Nous devons vérifier le contenu et les références avant la présentation.

Pour conclure, ce projet nous a permis de relier HTML, CSS et JavaScript dans un même site. Il montre que l'IA peut être utile, mais que ses résultats doivent être contrôlés et que son utilisation demande du recul. Merci de votre attention.

## Informations à retenir

- Le site est publié. Il n'y a pas de tâche de publication restante.
- Le compteur de visites utilise `localStorage` : il compte les ouvertures dans le navigateur courant, pas les visites globales de tous les utilisateurs.
- Les compteurs de clics et de temps repartent à zéro à chaque chargement de page.
- Les informations et les sources doivent être relues et vérifiées par les auteurs du projet.
