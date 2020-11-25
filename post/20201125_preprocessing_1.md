---
date: 20201124
url: preprocessing-1
title: Comment avoir une vision d'ensemble de ses données ?
static: img
twitter_summary: "Comment avoir une vision d'ensemble de ses données ?"
twitter_text: "Vous voulez une vision d'ensemble de vos données ? #IntelligenceArtificielle #IA #Deeplearning #Keras #python #fr #100DaysOfMLCode #multijunet"
---

Comme je l'ai déjà évoqué, avoir **de bonnes données** en entrée est une condition nécessaire pour faire du **machine learning** ou bien du **deep learning**.  

J'aime avoir une **vision d'ensemble** de ces données, quand cela est possible.  

Pour cela, je me base sur la librairie **pandas**.

Si je prend l'exemple du **dataset _iris_** de **sklearn**, on peut facilement afficher des informations sur les données :

|       |          0 |          1 |        2 |          3 |
|:------|-----------:|-----------:|---------:|-----------:|
| count | 150        | 150        | 150      | 150        |
| mean  |   5.84333  |   3.05733  |   3.758  |   1.19933  |
| std   |   0.828066 |   0.435866 |   1.7653 |   0.762238 |
| min   |   4.3      |   2        |   1      |   0.1      |
| 25%   |   5.1      |   2.8      |   1.6    |   0.3      |
| 50%   |   5.8      |   3        |   4.35   |   1.3      |
| 75%   |   6.4      |   3.3      |   5.1    |   1.8      |
| max   |   7.9      |   4.4      |   6.9    |   2.5      |

On retrouve donc le nombre d'enregistrement, la moyenne, l'écart type, la valeur minimum et maximum de chaque champ.  
Ainsi que le _percentille_ à 25, 50 et 75%.  

Pour afficher toutes ces informations, il faut dans un premier temps créer un _DataFrame_.

> import pandas as pd  
> x_pandas = pd.DataFrame(x_train)

Puis demander l'affichage de ces valeurs:

> x_pandas.describe()

# A toi !

N'oublie pas de t'**[inscrire par email][0]** pour ne pas rater les prochains épisodes.

[0]: {{"page//email.md"|yasifipo}}
