# Conway’s Game of Life — Projet POO (C++ / SFML)

## Simulation du Jeu de la Vie de Conway en C++ orienté objet, avec :

- Mode console

- Mode graphique SFML

- Tests unitaires

- Chargement depuis fichier

- Interface 8-bit rétro

- Édition manuelle + patterns

- Contrôle de la vitesse

- Musique (SFML Audio)

















📁 Structure du projet :

ProjetPOO/
│
├── Assets/
│   ├── font.ttf
│   ├── music1.ogg
│   └── music2.ogg
│   └── test.txt
│
├── include/
│   ├── Cell.hpp
│   ├── Grid.hpp
│   ├── Rule.hpp
│   ├── Game.hpp
│   ├── GridTopology.hpp
│   ├── InitialStateLoader.hpp
│   ├── ConsoleRunner.hpp
│   └── SfmlRunner.hpp
│
├── src/
│   ├── main.cpp
│   ├── Cell.cpp
│   ├── Grid.cpp
│   ├── Rule.cpp
│   ├── Game.cpp
│   ├── GridTopology.cpp
│   ├── InitialStateLoader.cpp
│   ├── ConsoleRunner.cpp
│   ├── SfmlRunner.cpp
│   └── Tests.cpp
│
├── game_of_life.exe
└── README.md



⚙️ Prérequis :

- Compilateur C++17

- Bibliothèque SFML (graphics, window, system, audio)

- Windows (MSYS2/MinGW) ou Linux

- Installation SFML (MSYS2) :

       pacman -S mingw-w64-x86_64-sfml




🛠️ Compilation :

Ouvrir le terminal MSYS2 MINGW64 et Executer la commandes ci-dessous :

          g++ src/*.cpp \
    -Iinclude \
    -o game_of_life \
    -std=c++17 \
    -lsfml-graphics -lsfml-window -lsfml-system -lsfml-audio




▶️ Exécution :

🔹 Mode Graphique :
        
        ./game_of_life assets/test.txt gui

🔹 Mode Console :

        ./game_of_life test.txt console 10

- test.txt : fichier d’état initial

- console : mode console

- 10 : nombre d’itérations (Choisir le nombre quon veut)



📄 Format du fichier test.txt :

.....
..1..
....1
.....
..1..

- 1 = cellule vivante

- . = cellule morte



🎮 Commandes du jeu :



Écran titre :

- ENTER / clic sur "START" : aller au menu principal
- "SETTINGS" : modifier les touches
- "CREDITS" : afficher les crédits
- ESC : quitter le jeu

Menu :

- HAUT / BAS : naviguer

- ENTRÉE : valider

- 1 / 2 / 3 : musique

- ECHAP : quitter

Mode Jeu :

- ESPACE : Pause / Play

- ← / → : modifier la vitesse

- M : revenir au menu

- ECHAP : quitter

Mode Édition :

- CLIC GAUCHE : poser/supprimer cellule

- Touches patterns : ajouter des formes

- ESPACE : lancer la simulation

- M : menu




🧠 Architecture Orientée Objet :

- Cell → état d’une cellule

- Grid → grille de cellules

- Rule → règles de Conway

- Game → moteur de simulation

- GridTopology → voisinage

- ConsoleRunner → interface texte

- SfmlRunner → interface graphique




🌟 Fonctionnalités implémentées (conforme a la demande du projet) :

- Chargement depuis fichier
- Simulation automatique
- Arrêt possible par nombre d’itérations
- Mode console
- Mode graphique
- Tests unitaires
- Placement de constructions
- Contrôle de la vitesse
- Interface POO complète



Tests unitaires :


Le projet intègre un module de tests unitaires permettant de vérifier automatiquement le bon fonctionnement des règles du Game of Life.

Les tests sont définis dans le fichier :

       src/Tests.cpp

Ils sont exécutés automatiquement au lancement du programme, avant l’exécution normale du jeu (mode console ou graphique).

🔍 Tests implémentés

Les tests suivants sont actuellement vérifiés :

Mort d’une cellule isolée
Une cellule vivante sans voisins doit mourir (sous-population).

Stabilité d’un bloc 2×2
Une structure stable doit rester inchangée après une itération.

Oscillation d’un blinker
Le blinker doit alterner correctement entre forme verticale et horizontale (période 2).

Déplacement d’un glider
Le glider doit continuer à exister après plusieurs générations.

Chaque test utilise des assertions (assert) pour vérifier automatiquement que l’état final de la grille correspond au résultat attendu.


▶️ Exemple d’exécution des tests :

Lors du lancement du programme, l’affichage suivant apparaît dans la console :

==== Lancement des tests unitaires ====
  - Cellule vivante isolee meurt ... OK
  - Bloc 2x2 reste stable ... OK
  - Blinker oscille correctement ... OK
  - Glider se deplace dans la grille ... OK
Tous les tests unitaires sont passes avec succes.



👨‍💻 Auteur :

Projet réalisé dans le cadre d’un Projet de Programmation Orientée Objet
Langage : C++17
Librairie graphique : SFML





     
