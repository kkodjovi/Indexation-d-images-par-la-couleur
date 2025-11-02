# Indexation d’images par la couleur

L’objectif de ce projet est d’**indexer une image donnée** `I` afin de **retrouver les images les plus similaires** à `I` en se basant sur leur **histogramme de couleur**.\
Cette indexation sera basée sur la quantification des couleurs et la comparaison d’histogrammes pour mesurer la similarité entre images.


## Voici le processus détaillé étape par étape


-   **Quantification des couleurs**\
    Réduction du nombre de valeurs possibles par composante RGB (en gardant les 2 bits de poids fort), créant ainsi des images codées sur 6 bits et donc 64 valeurs possibles.

-   **Histogramme de couleur**\
    Calcul de l’histogramme correspondant à chaque quantifiée

-   **Indexation des images**\
    Application du processus sur toutes les images d’un répertoire pour générer une matrice contenant l’ensemble des histogrammes.

-   **Recherche d’images similaires**\
    Calcul de similarité entre histogramme basé sur ***l'intersection d'histogrammes***. Puis recherche des ***5 images les plus proches*** d'une image I.

-   **Variante (3 bits par composante)**\
    Réalisation du même processus avec 3 bits de poids fort par couleur (512 valeurs possibles) et comparaison des résultats obtenus.