## Bibliothèque Dynamique libGeometry.so

Cette bibliothèque regroupe plusieurs fichiers contenant du code en C++ qui génèrent des formes géométriques.

Pour mieux structurer les données de chaque forme géométrique, on a eu recours à la Programmation Orientée Objet avec le langage C++.

À partir de ces fichiers .cpp et .hpp, on génère des fichiers .o pour la construction de la bibliothèque à partir des commandes suivantes :

g++ -fPIC -c *.cpp:

Cette commande utilise le compilateur C++ g++ pour compiler tous les fichiers *.cpp du dossier actuel.
L'option -fPIC indique à g++ de compiler le code pour une utilisation partagée (Position-Independent Code). Cela est nécessaire pour créer une bibliothèque dynamique.
L'option -c indique à g++ de créer des fichiers objets (*.o) au lieu d'un exécutable.
L'astérisque (*) indique à g++ de compiler tous les fichiers *.cpp du dossier.

g++ -o libGeometry.so -shared *.o:

Cette commande utilise le compilateur C++ g++ pour lier les fichiers objets (*.o) générés dans la commande précédente et créer une bibliothèque dynamique nommée libGeometry.so.
L'option -o libGeometry.so indique à g++ le nom de la bibliothèque dynamique à créer.
L'option -shared indique à g++ de créer une bibliothèque dynamique.
L'astérisque (*) indique à g++ d'ajouter tous les fichiers *.o du dossier à la bibliothèque.
