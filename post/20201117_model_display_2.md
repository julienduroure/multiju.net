---
date: 20201117
url: model-display-2
title: Comment connaître le format d'entrée de ton modèle ?
static: img
twitter_summary: "Connaître le format d'entrée du modèle"
twitter_text: "Connaître le format d'entrée du modèle # IntelligenceArtificielle #IA #DL #keras  #python #fr #multijunet"
---

On va regarder le **modèle Keras** suivant :

```
Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
dense_3 (Dense)              (None, 300)               235500    
_________________________________________________________________
dense_4 (Dense)              (None, 100)               30100     
_________________________________________________________________
dense_5 (Dense)              (None, 10)                1010      
=================================================================
Total params: 266,610
Trainable params: 266,610
Non-trainable params: 0
_________________________________________________________________
```

On retrouve pleins d'informations, mais le **format d'entrée**, ce qui est attendu par le réseau, n'est pas affiché !  

Heureusement, on peut le retrouver facilement :

# Paramètres entraînables

Pour la **1ère couche**, on voit qu'il s'agit d'une couche *Dense* de **300 neurones**, et qu'il y a **235500 paramètres entraînables**.  

Un rapide calcul nous donne :

> 235500 / 300 = 785

Il y a donc 785 poids (_weights_) en entrée de cette couche. Un de ces poids correspond au **biais**.  

C'est donc que le format d'entrée est **784**. Cela tombe bien, c'est le nombre de pixels sur une **image 28*28**, comme dans le jeu de donnée **MNIST**.

Une prochaine fois, je te montrerai comment retrouver le format d'entrée depuis le modèle !

# A toi !

Tu veux poursuivre l'aventure ?  
**[Inscrit-toi][0]** pour ne rien rater des prochaines escales !
