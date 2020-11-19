---
date: 20201119
url: model-display-4
title: Comment nommer les couches dans un modèle Keras ?
static: img
twitter_summary: "Comment nommer les couches dans un modèle Keras ?"
twitter_text: "Comment nommer les couches dans un modèle Keras ? #IntelligenceArtificielle #IA #Deeplearning #Keras #python #fr #multijunet"
---

Comment mieux si retrouver au milieu de toutes ces couche ?


Si tu regardes le modèle suivant :

```
model_1 = Sequential([
               Dense(300, input_shape=(784,), activation='relu'),
               Dense(100, activation='relu'),
               Dense(10, activation='softmax')     
])
model_1.compile(loss='sparse_categorical_crossentropy', metrics=['accuracy'])
```

Son résumé est le suivant :

```
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
dense (Dense)                (None, 300)               235500    
_________________________________________________________________
dense_1 (Dense)              (None, 100)               30100     
_________________________________________________________________
dense_2 (Dense)              (None, 10)                1010      
=================================================================
Total params: 266,610
Trainable params: 266,610
Non-trainable params: 0
_________________________________________________________________
```

En tout cas, c'est le cas la première fois que je définis un modèle nommé _model_1_.  

Car la deuxième fois, cela donnera :

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

On voit que le nom du modèle et le **nom des couches** changent. Ici, le modèle est simple, donc on arrive à **s'y retrouver**.  
Mais pour un modèle plus complexe, je te conseille de **nommer les couches** :

```
model_1 = Sequential([
               Dense(300, input_shape=(784,), activation='relu', name='input'),
               Dense(100, activation='relu', name='hidden'),
               Dense(10, activation='softmax', name='output')     
], name="MonModele")
model_1.compile(loss='sparse_categorical_crossentropy', metrics=['accuracy'])
```

Cela donne :

```
Model: "MonModele"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
input (Dense)                (None, 300)               235500    
_________________________________________________________________
hidden (Dense)               (None, 100)               30100     
_________________________________________________________________
output (Dense)               (None, 10)                1010      
=================================================================
Total params: 266,610
Trainable params: 266,610
Non-trainable params: 0
_________________________________________________________________
```

Y compris si je redéfini mon modèle _model_1_.

On verra une prochaine fois quel est l'**avantage** pour une couche d'avoir un **nom constant**.

# A toi !

N'oublie pas de t'**[inscrire par email][0]** pour ne pas rater les prochains épisodes.

[0]: {{"page//email.md"|yasifipo}}
