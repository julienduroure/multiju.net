---
date: 20201126
url: parameters-hyperparameters
title: Quelle est la différence entre paramètre et hyperparamètre ?
static: img
twitter_summary: "Quelle est la différence entre paramètre et hyperparamètre ?"
twitter_text: "Quelle est la différence entre paramètre et hyperparamètre ? #IntelligenceArtificielle #IA #Deeplearning #Keras #python #fr #100DaysOfMLCode #multijunet"
---

Tu as sans doute déjà entendu parler de ces deux termes :

**paramètre** et **hyperparamètre**

* Le premier, paramètre, définit toutes les variables qui sont **entraînables**, donc **modifiées** lors de l'apprentissage. Ce soit donc tous les **poids** liés aux neurones.

* Le deuxième, **hyperparamètre**, sont tous les paramètres qui ne sont **pas modifiés** pendant l’entraînement, mais qui servent à **définir le modèle** : nombre de couches, nombre de neurones dans chaque couche, etc...

Par exemple, dans le **modèle simple** ci-dessous:

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

On voit qu'il y a **266610** paramètres. Ils correspondent à tous les poids entre les différents neurones des différentes couches.  

# A toi de jouer

N'oublie pas de t'**[inscrire par email][0]** pour ne pas rater les prochains épisodes.

[0]: {{"page//email.md"|yasifipo}}
