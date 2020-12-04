---
date: 20201204
url: callback-tensorboard
title: Comment générer des données pour tensorboard ?
static: img
twitter_summary: "Comment générer des données pour tensorboard ?"
twitter_text: "Comment générer des données pour tensorboard ? #IntelligenceArtificielle #IA #Deeplearning #tensorflow #tensorboard #python #fr #multijunet"
---
# Générer des données pour **tensorboard**

Tu l'as vu hier, pour afficher des données dans **tensorboard**, il faut avoir généré des *logs* pour que **tensorboard** puisse les lire.  

Ces **logs** sont générés par un **callback**.

Un **callback** est un code qui est exécuté à **chaque epoch**, ou à **chaque batch**, etc...

Un **callback** est soit défini par le développeur, soit tu peux également utiliser un callback déjà défini dans **keras**.

C'est le cas du **callback pour tensorboard**, il est déjà défini dans **keras**.

Il faut donc l'instancier :

```
tensorboard_callback = keras.callbacks.TensorBoard("./logs/run_1")
```

Puis passer ce ou ces callbacks lors de l'apprentissage, sous forme de _list_ :

```
model.fit(x_train, y_train, callbacks=[tensorboard_callback])
```

Il faut définir un nom de répertoire différent pour chaque essai :

```
tensorboard_callback = keras.callbacks.TensorBoard("./logs/run_2")
```

Ensuite, on peut **lancer tensorboard**, où on pourra comparer les différents _runs_ (avec Google Colab par exemple) :

```
%load_ext tensorboard
%tensorboard --logdir ./logs
```

# A toi de jouer

N'oublie pas de t'**[inscrire par email][0]** pour ne pas rater les prochains épisodes.

[0]: {{"page//email.md"|yasifipo}}
