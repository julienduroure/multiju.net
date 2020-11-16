---
date: 20201116
url: model-display-1
title: Visualiser un modèle Keras
static: img
twitter_summary: "Visualiser un modèle Keras"
twitter_text: "Visualiser un modèle Keras ! #IA #IntelligenceArtificielle #DL #keras #python #fr #multijunet"

---
# Comment visualiser tes modèles Keras ?

Il existe plusieurs manières différentes de **visualiser les modèles Keras**.  

Aujourd'hui, je vais te parler du **plus simple** :

> model.summary()

Cela donne le résultat suivant :

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

C'est aussi simple que cela. Mais cela soulève quelques questions :

* Si j'ai un modèle assez conséquent, est ce que cela reste aussi **lisible** ?

Par exemple, le modèle ResNet152 fait **1092 lignes**. Je ne vous affiche que les dernières lignes ici.
(Je ne m'attarde pas ici sur le modèle, on aura l'occasion d'y revenir)  

```
conv5_block3_3_conv (Conv2D)    (None, 7, 7, 2048)   1050624     conv5_block3_2_relu[0][0]        
__________________________________________________________________________________________________
conv5_block3_3_bn (BatchNormali (None, 7, 7, 2048)   8192        conv5_block3_3_conv[0][0]        
__________________________________________________________________________________________________
conv5_block3_add (Add)          (None, 7, 7, 2048)   0           conv5_block2_out[0][0]           
                                                                 conv5_block3_3_bn[0][0]          
__________________________________________________________________________________________________
conv5_block3_out (Activation)   (None, 7, 7, 2048)   0           conv5_block3_add[0][0]           
__________________________________________________________________________________________________
avg_pool (GlobalAveragePooling2 (None, 2048)         0           conv5_block3_out[0][0]           
__________________________________________________________________________________________________
predictions (Dense)             (None, 1000)         2049000     avg_pool[0][0]                   
==================================================================================================
Total params: 60,419,944
Trainable params: 60,268,520
Non-trainable params: 151,424
__________________________________________________________________________________________________
```

On peut voir qu'il y a une colonne supplémentaire, dont le nom est _Connected to_, qui indique que le modèle n'est pas **séquentiel**, contrairement au 1er exemple. On aura l'occasion d'y revenir !  

1092 lignes, c'est beaucoup, et pas forcément très **lisible**. Heureusement, il existe d'autres moyens d'afficher les modèles. Mais ça, ce sera pour une autre fois.

En attendant, n'oublie pas de t'**[inscrire par email][0]** pour ne pas rater les prochains épisodes.

[0]: {{"page//email.md"|yasifipo}}
