---
date: 20201202
url: matrice-de-confusion
title: Qu'est ce qu'une matrice de confusion ?
static: img
twitter_summary: "Qu'est ce qu'une matrice de confusion ?"
twitter_text: "Qu'est ce qu'une matrice de confusion ? #IntelligenceArtificielle #IA #Deeplearning #statistique #python #fr #100DaysOfMLCode #multijunet"
---

Une **matrice de confusion** est une matrice qui permet de mesurer la **qualité d'un modèle de classification**.

Sur **les lignes** de la matrice, on trouve les classes réelles.  
Sur **les colonnes**, on retrouve les prévisions calculées par le modèle.  

# Exemple d'une classification binaire

Dans le cas d'**une classification binaire**, on aura une **matrice 2x2** :

| | prédiction classe 0  | prédiction classe 1  |
|-|:-:|:-:|
| classe 0  | 32 | 3 |
| classe 1 | 2 | 27 |

Il y a dans cet exemple **64 échantillons**.  
35 appartiennent à la classe 0 (ligne 0), et 29 à la classe 1 (ligne 1).  

Le modèle en a détecté 34 dans la classe 0 (colonne 0), et 30 dans la classe 1 (colonne 1).  

Le modèle a détecté correctement 32 échantillons de la classe 0, et 27 échantillons de la classe 1.  
On peut lire les données correctement prédites en regardant **la diagonale** de la matrice.

Le modèle a prédit 3 échantillons dans la classe 1 alors que ce sont des données de la classe 0. On parle de **faux positifs**.

Le modèle a prédit 2 échantillons dans la classe 0 alors qu'il s'agissait de données de la classe 1. On parle de **faux négatifs**.

# Comment construire une matrice de confusion ?

Le plus simple est d'utiliser l'outil mis à disposition dans la bibliothèque *sklearn* :

```
from sklearn.metrics import confusion_matrix
```

On peut l'appeler ensuite de cette manière :

```
matrice_confusion = confusion_matrix(y_reel, y_predit)
```

Il faut donc passer en paramètres :
* En premier **les valeurs réels** des classes, le plus souvent il s'agit donc des labels du *dataset*
* Puis **les valeurs prédites** par le modèle

On obtient donc le résultat suivant, par exemple:

```
print(matrice_confusion)

array([[40,  2],
       [ 0, 72]])
```

(Ici, on a donc 2 faux positifs, et aucun faux négatifs)

# A toi !

Tu veux poursuivre l'aventure ?  
**[Inscrit-toi][0]** pour ne rien rater des prochaines escales !

[0]: {{"page//email.md"|yasifipo}}
