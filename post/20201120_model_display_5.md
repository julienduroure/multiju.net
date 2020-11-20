---
date: 20201120
url: model-display-5
title: Comment retrouver une couche particulière ?
static: img
twitter_summary: "Comment retrouver une couche particulière ?"
twitter_text: "Comment retrouver une couche particulière dans un modèle Keras ? #IntelligenceArtificielle #IA #Deeplearning #Keras #python #fr #multijunet"
---

On peut accéder à 1ère couche avec :

> model.layers\[0\]

Je t'en ai parlé déjà, on peut donner un **nom à une couche**, ce qui permet d'avoir un **nom fixe**.  
Dans ce cas là, on peut récupérer la couche de la manière suivante :

> model.get_layer("input")

Et tu peux retrouver le **format d'entrée** avec l'attribut _input_shape_.

> model.get_layer("input").input_shape

Cela donne :

> (None, 784)

On retrouve bien le format d'entrée 784. Le _None_ ici correspond à la taille du _Batch Size_, qui n'est pas connu à l'avance.

# A toi !

N'oublie pas de t'**[inscrire par email][0]** pour ne pas rater les prochains épisodes.

[0]: {{"page//email.md"|yasifipo}}
