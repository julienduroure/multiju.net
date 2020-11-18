---
date: 20201118
url: model-display-3
title: Afficher plus de détails sur le modèle
static: img
twitter_summary: "Afficher plus de détails sur le modèle"
twitter_text: "Afficher plus de détails sur le modèle # IntelligenceArtificielle #IA #Deeplearning #keras #python #fr #multijunet"
---

Regardons les 2 modèles suivants:

```
model_1 = Sequential([
               Dense(300, input_shape=(784,), activation='relu'),
               Dense(100, activation='relu'),
               Dense(10, activation='softmax')     
])
model_1.compile(loss='sparse_categorical_crossentropy', metrics=['accuracy'])
```
Voici son résumé :

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

Et le deuxième :

```
model_2 = Sequential([
               Input(shape=(784,)),
               Dense(300),
               Activation(keras.activations.relu),
               Dense(100),
               Activation(keras.activations.relu),
               Dense(10),
               Activation(keras.activations.softmax)   
])
model_2.compile(loss='sparse_categorical_crossentropy', metrics=['accuracy'])
```

Et son résumé :

```
Model: "sequential_3"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
dense_11 (Dense)             (None, 300)               235500    
_________________________________________________________________
activation_1 (Activation)    (None, 300)               0         
_________________________________________________________________
dense_12 (Dense)             (None, 100)               30100     
_________________________________________________________________
activation_2 (Activation)    (None, 100)               0         
_________________________________________________________________
dense_13 (Dense)             (None, 10)                1010      
_________________________________________________________________
activation_3 (Activation)    (None, 10)                0         
=================================================================
Total params: 266,610
Trainable params: 266,610
Non-trainable params: 0
_________________________________________________________________
```

Les deux modèles sont **identiques**.  

Pour la définition du premier, on a utilisé une déclaration la plus condensée possible, là où on a définit plus de couches dans le deuxième, même si le résultat est similaire.  

On voit que le résumé est lui aussi différent, et reflète bien ces changements.

# A toi de jouer

N'oublie pas de t'**[inscrire par email][0]** pour ne pas rater les prochains épisodes.

[0]: {{"page//email.md"|yasifipo}}
