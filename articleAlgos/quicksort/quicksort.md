# Tri rapide (quicksort ou Qsort)



## Présentation du Tri rapide : 

Le principe de ce tri est assez original mais sur le moment difficile à comprendre.
Pourtant il est trés efficace pour trier des informations désordonnées et donne de bons résulats.

-> Vous rencontrerez sûrement à un moment ou à un autre.

MAIS par contre pour une liste presque triée: il faudra trouver une autre solution de tri (selection ou autre) 

_____________
Quel intérêt ? Ces points forts...

* C'est l'algorithme le plus utilisé car c'est en pratique un des tris les plus rapides, et donc un des plus utilisés.
* Son crédo: diviser pour régner ! (en gros)

* Sa principale utilisation:
Souvent donc pour les tableaux, mais peut aussi être adapté aux listes.

* Les pires des cas est en effet peu probable avec cet algo, lorsqu'il est correctement mis en œuvre avec l'utilisation de ce tri.

_____________

Par contre, son gros point noir:
- Un gros désavantage théorique (eh oui comprendre son fonctionnement est assez hard), 
- Il existe de nombreuses versions de quickSort qui sélectionnent pivot de différentes manières.




## comment cela fonctionne (bien comprendre): 

En théorie ça donne donc:
-> La cible des partitions est, étant donné: un tableau et un élément x du tableau: comme pivot (la valeur donc), 
-> place x à sa position correcte dans le tableau trié 
-> et place tous les éléments plus petits (inférieurs à x) avant x 
-> et tous les éléments supérieurs (supérieurs à x) après X. 

La méthode donc consiste à placer un élément du tableau (appelé pivot (=valeur)) à sa place définitive, en permutant tous les éléments de telle sorte que
tous ceux qui sont inférieurs au pivot soient à sa gauche 
et que tous ceux qui sont supérieurs au pivot soient à sa droite.

Cette opération s'appelle le partitionnement. 

Pour chacun des sous-tableaux:
on définit un nouveau pivot et on répète l'opération de partitionnement. 

Ce processus est répété récursivement, jusqu'à ce que l'ensemble des éléments soit trié.


## TESTER LE SUJET :) : 
procédure à réaliser avec des cartes:

(à rédiger car simulation en temps réel trop rapide)




_________________________________________________________________________________

## en savoir plus: 

Cet algo a été inventé par C.A.R. Hoare en 1961.

https://www.youtube.com/watch?v=PgBzjlCcFvc


Source : [GEEKFORGEEKS](https://www.youtube.com/watch?v=PgBzjlCcFvc) - 
         [Turoriel](http://sdz.tdct.org/sdz/le-tri-par-tas.html)

un exemple du Tri rapide avec un gif : ![](images/xxxxxxx.gif)

_________________________________________________________________________________

## en pratique, voici un exemple : 

