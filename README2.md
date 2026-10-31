# Récapitulatif des modifications du site

Ce fichier liste les changements apportés au projet depuis sa première version.

## Structure du site

- Conservation de deux pages HTML reliées entre elles :
  - `index.html` : présentation du sujet et interactions ;
  - `contenu1.html` : avantages, points de vigilance, tableau, sources et conclusion.
- Les deux pages utilisent maintenant une seule feuille de style : `contenu.css`.
- Suppression de `contenu2.css` afin de respecter la demande d'une seule feuille CSS.
- Ajout de `lang="fr"`, de l'encodage UTF-8 et de la configuration pour l'affichage mobile.

## Page d'accueil — `index.html`

- Présentation du thème : l'impact de l'intelligence artificielle sur les métiers de l'informatique.
- Image illustrant le sujet, redimensionnée et cliquable pour ouvrir la deuxième page.
- Liste des changements liés à l'IA.
- Lien ancre vers le schéma explicatif.
- Résumé des avantages et des inconvénients.
- Devinette avec réponse masquée, révélée au clic.
- Définition du terme « IA » visible au survol de la souris.
- Schéma en quatre étapes : collecte de données, entraînement, résultat, évaluation et amélioration.
- Lien vers les sources présentées sur la deuxième page.
- Réponse de la devinette révélée au clic.
- Script JavaScript placé en bas de page et commenté.

## Deuxième page — `contenu1.html`

- Réécriture des grands paragraphes en sections plus courtes.
- Présentation des avantages et des points de vigilance de l'IA.
- Tableau comparatif avec titres de colonnes centrés.
- Un unique bloc discret de compteurs (visites, clics et temps), placé en bas de cette page.
- Références externes sur la définition de l'IA, l'emploi et l'énergie.
- Mention transparente de l'utilisation d'une IA comme aide au code et à la rédaction.
- Conclusion enrichie placée à la fin de la page.
- Icône maison réduite et cliquable pour revenir à l'accueil.
- Commentaires ajoutés aux parties importantes du HTML et du JavaScript.

## Feuille de style — `contenu.css`

- Application d'un style commun aux deux pages.
- Fond sombre animé avec plusieurs dégradés.
- Amélioration de la lisibilité par les couleurs, espacements, bordures et encadrés.
- Taille de l'image d'accueil réduite sans affecter l'icône maison.
- Mise en forme de la liste, des boutons, des sections, du schéma et du tableau.
- Effet visuel au survol des boutons.
- Affichage/masquage des réponses et définitions avec des classes CSS.
- Adaptation de la grille aux écrans étroits.
- Commentaires français ajoutés aux règles moins évidentes.

## Consignes facultatives non ajoutées

La fiche cite la météo, la température, la vitesse du vent, les sons et les webcams comme exemples facultatifs. Ces éléments n'ont pas été ajoutés ; le site ne présente donc pas de valeurs météo inventées ni de données qui ne viennent pas d'une source réelle.

## Travail restant pour le dossier de rendu

- Publier le site et noter son adresse.
- Faire des captures d'écran des pages.
- Préparer un diaporama.
- Répéter la présentation orale : cinq minutes par élève, soit environ dix minutes pour le binôme.

## Limites à connaître

- Le compteur de visites utilise `localStorage` dans le navigateur courant ; ce n'est pas un total partagé entre tous les visiteurs.
- Les compteurs de clics et de temps repartent à zéro au rechargement de la page.
- Les informations et les sources doivent être relues et vérifiées par les auteurs du projet.
