# EDA

## Sources

Le détail de mon travail (documenté en temps réel) se trouve dans ./scraper/scraper.ipynb et dans ./data_mining/data_mining.ipynb

## Questionnement

Est-il possible à partir des palmarès des précédentes éditions des 24h du mans, de prévoir le futur vainqueur ?

## Explication / raisonnement

Le scraper m'a pris plus de temps que prévu et par manque de temps, je n'ai pas pu finaliser la partie d'analyse du projet ni même commencer la partie machine learning que j'avais prévu.

Pour la partie de preprocessing, j'ai commencé à retravailler mon dataframe pour le rendre exploitable.
Mais comme je n'ai pas eu le temps de finir, je vais décrire ici ce que j'avais initialement prévu.

Premièrement, étant donné que presque toutes mes données sont des strings,
Il faut que je les transforme en valeur analysable.
Pour la colonne "engine" par exemple, j'ai des valeurs comme celle-ci par exemple "Moteur Bentley L4 2996cc"
Dans laquelle je peux retrouver la cylindrée entre autres, mais cette donnée ne m'est pas très utile, car je peux déjà catégoriser ce moteur grâce à la colonne "category" (celui-ci est dans la catégorie "2001 a 3000")

En revanche, d'autres colonnes peuvent être intéressantes à travailler comme la colonne "race_mean" par exemple de laquelle je peux extraire un float et que je pourrais mettre en comparaison avec la colonne "race_max_speed" et "rank" pour savoir s'il vaut mieux avoir une moyenne élevée ou une vitesse maximum élevée pour gagner la course par exemple.

Je peux aussi me servir de la colonne "try_rank" pour essayer de voir s'il existe une corrélation entre le classement aux essais et la victoire final.

Dans tous les cas, je suis déçu de ne pas pouvoir pousser plus loin mon travail. (que je reprendrai très probablement plus tard dans l'année)

## Conclusion

Il est probablement possible d'estimer une victoire, mais il faudrait croiser les palmarès de tous les championnats par saisons et d'effectuer le même travail d'analyse ce qui est un travail colossal.
Avec mon jeu de données, il me serait possible de sortir une estimation, mais elle ne sera que très peut précise