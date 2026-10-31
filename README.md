# Mini-projet NSI — L'impact de l'IA sur les métiers de l'informatique

## Présentation du site

Le site comporte deux pages HTML reliées entre elles :

- `index.html` présente le sujet, une liste, une image cliquable, une ancre, une devinette et un schéma explicatif.
- `contenu1.html` développe les avantages et les points de vigilance, avec un tableau, les sources et une conclusion.
- `contenu.css` contient le style commun et la première feuille de style.
- `contenu2.css` est la feuille du deuxième élève : elle importe le style commun et ajoute des styles propres à la deuxième page.

Les éléments facultatifs de la fiche — météo, température, vitesse du vent, sons ou webcam — ne sont pas ajoutés. Le site ne présente ainsi aucune donnée de démonstration comme une information réelle.

## Vérification des consignes

- [x] Deux pages distinctes reliées par des liens.
- [x] Deux feuilles CSS pour deux élèves ; le style commun est réutilisé et chaque feuille contribue à la mise en forme.
- [x] Un titre, une image liée au sujet, une liste, un tableau, des liens internes et externes, une image cliquable, une source et une ancre.
- [x] Compteur de clics, temps passé et visites sur chacune des pages.
- [x] Réponse à la devinette affichée au clic.
- [x] Définition du terme « IA » affichée au survol.
- [x] CSS et JavaScript commentés en français.
- [ ] Pour le dossier de rendu : ajouter l'adresse du site publié, des captures d'écran et un diaporama.
- [ ] Préparer une présentation orale de cinq minutes par élève.

Les compteurs de visites utilisent `localStorage` : ils comptent les ouvertures dans le navigateur courant, pas les visites globales de tous les utilisateurs. Les compteurs de clics et de temps repartent à zéro à chaque chargement de page.

## Proposition de texte pour l'oral

Bonjour, nous allons vous présenter notre mini-site réalisé pour le projet de NSI. Nous avons choisi comme sujet l'impact de l'intelligence artificielle sur les métiers de l'informatique. L'IA peut aider à écrire du code et à analyser des données, mais elle transforme aussi les tâches et les compétences attendues. Nous avons donc voulu présenter ses possibilités et les points auxquels il faut rester attentif.

Notre site est composé de deux pages HTML et de deux feuilles de style, une par élève. La première page, `index.html`, introduit le thème. Elle comprend une image cliquable qui conduit vers la deuxième page, une liste de changements liés à l'IA, ainsi qu'un lien ancre. Une ancre est un lien qui fait défiler la page jusqu'à un élément précis, identifié ici par `details`.

La première page contient aussi un schéma simplifié du fonctionnement d'une IA. On peut le présenter en quatre étapes. D'abord, on rassemble des données, comme des textes ou des images. Ensuite, un algorithme utilise des exemples pour entraîner un modèle et repérer des régularités. Le modèle produit ensuite un résultat lorsqu'il reçoit une nouvelle donnée ou une demande. Enfin, on évalue ce résultat et on cherche à corriger les erreurs. Ce schéma est volontairement général : les techniques exactes varient selon le type d'IA.

La deuxième page détaille les avantages et les points de vigilance. L'IA peut faire gagner du temps sur certaines tâches, aider à analyser un grand volume de données et assister les développeurs. En revanche, elle peut produire des erreurs ou reproduire des biais présents dans les données. Certaines tâches ou certains métiers peuvent évoluer. Les systèmes d'IA nécessitent aussi du matériel informatique et de l'énergie. Le tableau de la page résume ces deux aspects. Les textes restent courts pour distinguer rapidement les idées, puis le tableau les met en regard sans prétendre donner une réponse unique sur l'avenir de tous les métiers.

Nous avons utilisé HTML pour structurer le contenu. Les balises `<h1>` et `<h2>` organisent les titres, `<p>` les paragraphes, `<ul>` ou `<ol>` les listes et `<table>` le tableau. La balise `<a>` crée des liens, tandis que `<img>` affiche une image. L'attribut `alt` décrit cette image si elle ne s'affiche pas ou pour les outils d'accessibilité. Les identifiants `id` servent à cibler un élément précis, et les classes `class` permettent d'appliquer les mêmes styles à plusieurs éléments.

Le fichier `contenu.css` définit le style commun des deux pages. Il règle notamment la police, les couleurs, les marges, les bordures, les tailles et les espacements. Le fond sombre est composé de plusieurs dégradés, et une animation les déplace lentement. Les sélecteurs comme `h1` ciblent une balise, `.mini-section` cible une classe et `#maison` cible un identifiant. Le sélecteur `:hover` permet d'appliquer un style quand le pointeur passe sur un élément. Une règle `@media` adapte la présentation aux petits écrans. Comme nous sommes deux, `contenu2.css` importe les règles communes avec `@import`, puis ajoute une alternance légère de couleur aux lignes du tableau et une couleur aux titres de section. Cette organisation évite de recopier toutes les règles communes dans un deuxième fichier.

Pour la présentation, nous pouvons montrer d'abord les deux pages et faire les actions en direct : cliquer sur l'image pour naviguer, utiliser le lien ancre, révéler la réponse et passer la souris sur « IA ». Nous pouvons ensuite montrer les compteurs, le tableau et les sources. Ces démonstrations permettent de vérifier que le site ne contient pas seulement du texte statique.

Le JavaScript ajoute les interactions. Les compteurs de clics augmentent quand on appuie sur leur bouton. Le temps passé est actualisé chaque seconde grâce à `setInterval`. Les visites sont enregistrées dans `localStorage`, une mémoire du navigateur qui conserve une valeur après fermeture de la page. Ce compteur est local à un navigateur : il ne représente pas le nombre total de visiteurs du site.

Dans le code, `getElementById` récupère un élément HTML à partir de son identifiant, puis `textContent` change le nombre affiché sans reconstruire toute la page. `Number` transforme la valeur enregistrée sous forme de texte en nombre afin de pouvoir l'incrémenter. La variable `clics` est propre au chargement en cours, tandis que le compteur des visites est sauvegardé. Les deux pages ont des identifiants et des clés de stockage différents pour ne pas mélanger leurs compteurs. Cela permet aussi de discuter d'une limite : effacer les données du navigateur réinitialise les visites enregistrées.

La devinette utilise JavaScript pour ajouter ou retirer la classe CSS `visible` quand on clique sur le bouton. La réponse est donc masquée au départ, puis affichée. La définition du mot « IA » utilise une autre méthode : elle apparaît au survol grâce au CSS.

Pour les informations, nous avons ajouté des liens vers des sources sur la définition de l'IA, l'emploi et l'énergie. Une IA a servi d'aide à la structuration et aux commentaires du code ainsi qu'à la préparation d'une première version du texte. Nous devons vérifier le contenu et les références avant la présentation.

Pour conclure, ce projet nous a permis de relier HTML, CSS et JavaScript dans un même site. Il montre que l'IA peut être utile, mais que ses résultats doivent être contrôlés et que son utilisation demande du recul. Merci de votre attention.

## Dossier à remettre

La fiche demande de remettre un dossier comprenant :

1. l'adresse du site publié ;
2. des captures d'écran du site ;
3. un diaporama pour accompagner la présentation orale ;
4. les scripts du projet, largement commentés.

Nous sommes deux : la présentation orale doit donc durer cinq minutes par élève, soit environ dix minutes au total. Le texte ci-dessus sert de base et peut être partagé entre les deux élèves ; il faut le répéter et l'adapter à votre débit de parole.
