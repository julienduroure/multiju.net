---
date: 20201203
url: lancer-tensorboard
title: Comment lancer Tensorboard ?
static: img
twitter_summary: "Comment lancer Tensorboard ?"
twitter_text: "Comment lancer Tensorboard ? #IntelligenceArtificielle #IA #Deeplearning #tensorflow #tensorboard #python #fr #multijunet"
---

Et tout d'abord, qu'est ce que **Tensorboard** ?

**Tensorboad** est un outil de **visualisation interactive** des données d’entraînement.

Il permet (entre autres):
* de visualiser les courbes d'apprentissage, et de pouvoir les comparer, entre plusieurs entraînement différents.
* de visualiser diverses analyses statistiques de tes modèles
* de visualiser les images, sons, textes, générés par ton modèle
* de visualiser des données multi-dimensionnelles projetées en 3D

Bref, tu l'auras compris, c'est un **outil assez puissant** qui permet de réaliser et **visualiser énormément de choses différentes**.

Pour aujourd'hui, on va voir comment lancer **tensorboard**. L'outil est tellement varié, qu'on pourra y revenir pour expliquer certaines fonctionnalités, les unes après les autres.

Bonne nouvelle : **Tensorboard** est directement disponible avec **Tensorflow** !

* Si as installé **Tensorflow** sur ton ordinateur, tu peux lancer _Tensorboard_ de la manière suivante :

```
tensorboard --logdir /lien/vers/logs/
```

Cela lance **un serveur**, accessible par défaut sur le **port 6006** :

> http://localhost:6006/

* Si tu utilises **Tensorflow** sur **Google Colab**, tu peux lancer **Tensorboard** comme ceci :

```
%load_ext tensorboard
%tensorboard --logdir /lien/vers/logs/
```

**Tensorboard** sera affiché dans le **résultat de la cellule**.

Comme tu peux le voir, **tensorboard** nécessite un répertoire de logs, qui doit avoir été **généré lors de l'apprentissage**.

Tu pourras le découvrir demain, il existe heureusement un **callback** qui permet de **générer automatiquement le contenu** de ce répertoire.

# A toi !

N'oublie pas de t'**[inscrire par email][0]** pour ne pas rater les prochains épisodes.

[0]: {{"page//email.md"|yasifipo}}
