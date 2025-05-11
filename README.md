# README - Jeu Plateforme avec Qt/C++

## Description

Ce projet est un petit jeu de plateforme 2D développé en C++ avec Qt. Le joueur contrôle un personnage (par défaut Spider-Man), qui peut se déplacer à gauche, à droite et sauter. Le but est de progresser sur des plateformes jusqu'à atteindre la fin du niveau. Un système de score est présent, augmentant à chaque plateforme atteinte.

Le jeu gère les collisions, la gravité, et une vue centrée dynamiquement sur le personnage. En cas de chute ou d'arrivée au bout du niveau, un message de victoire ou de défaite s'affiche.

## Fichiers principaux

* `MyScene.cpp / MyScene.h` : Gère la scène du jeu, les objets graphiques, la logique du jeu, le mouvement, la gravité, le score et les collisions.
* `MainWindow.cpp / MainWindow.h` : Initialise la fenêtre principale, crée la vue principale et associe la scène.

## Fonctionnalités

* Affichage de plateformes fixes et mobiles
* Personnage pouvant se déplacer et sauter
* Saut uniquement si le personnage est sur une plateforme
* Gravitation permanente
* Texte dynamique affichant le score
* Affichage d'un message de victoire ou de défaite
* Bouton "Rejouer" en cliquant sur le message de fin de partie
* Vue qui suit automatiquement le personnage
* Animation du personnage (alternance d'images)

## Problème connu

Lorsqu'on clique sur "Rejouer" (après une défaite ou une victoire), la vue principale (`QGraphicsView`) ne se recentre pas automatiquement sur le personnage. Pour corriger cela manuellement, il faut appuyer une fois sur la flèche de déplacement vers la droite (`Qt::Key_Right`) pour recentrer la vue correctement.

Une solution d'amélioration serait de recentrer directement la vue sur le personnage dès que le jeu redémarre.

## Dépendances

* Qt 5 ou Qt 6 (modules QtWidgets, QtGui, QtCore)
* Fichiers images : plateformes, personnage (plusieurs versions pour l'animation), fond d'écran

## Lancement du jeu

1. Compiler le projet avec Qt Creator ou `qmake` + `make`
2. Lancer l'exécutable
3. Utiliser les touches suivantes :

   * Flèche droite : avancer
   * Flèche gauche : reculer
   * Flèche haut : sauter (uniquement si sur une plateforme)
   * Touche `P` : pause / reprendre le jeu

## Auteur

Projet développé à titre d'apprentissage en C++/Qt.

---

**Note** : Le code utilise des chemins relatifs pour les images (ex : `../spidermandevant.jpg`). Assurez-vous que les ressources soient bien présentes dans les bons dossiers.
