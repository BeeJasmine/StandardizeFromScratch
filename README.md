# StandardizeFromScratch

Ces notebook montrent, en détail, les calculs effectués par la fonction StandardScaler de ScikitLearn.
######   StandardiZationFromScratch.ipynb = sans numpy, _pure from scratch_
######   StandardScaler2.ipynb = avec numpy

#
#
Standardiser un jeu de donnée est une étape parfois nécessaire, voir primordiale, à la construction du modèle.

POUR RAPPEL: _La qualité des données **détermine** la qualité de notre modèle._

#

Le calcul de la standardisation ramène toutes nos valeurs observées à des valeurs donc dites standardisées

 == dont la moyenne est égale à 0 et le std est égale à 1.
 
 voir ![variable centrée réduite](https://fr.wikipedia.org/wiki/Variable_centr%C3%A9e_r%C3%A9duite)
 
 #
 #
 
Nous suivons les 3 étapes suivantes : 



1. on trouve la moyenne de chaque colonne :


- on somme l'ensemble des valeurs de cette colonne 
- puis on divise cette somme par le nombre de valeurs additionnées (la longueur de la colonne)

![Means](https://raw.githubusercontent.com/BeeJasmine/StandardizeFromScratch/master/Assets/formula_mean.png)


2. on trouve la standard deviation (l'écart-type) de chaque colonne
  l'écart type est la racine carrée de la variance :


_- Calculez la moyenne._
- Soustrayez de chaque observation la moyenne.
- Calculez le carré de chacune des autres observations.
- Additionnez ces résultats au carré.
- Divisez ce total par le nombre d'observations (la variance, S2).
- Utilisez la racine carrée positive (écart-type, S).


![stds](https://raw.githubusercontent.com/BeeJasmine/StandardizeFromScratch/master/Assets/formula_std.png)


3. avec les observations issues du jeu de données, nos moyennes et nos stds, on peut enfin obtenir le score Z :

![Z](https://raw.githubusercontent.com/BeeJasmine/StandardizeFromScratch/master/Assets/formula_standardization.png)

