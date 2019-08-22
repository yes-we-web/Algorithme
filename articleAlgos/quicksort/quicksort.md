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


Prenons une suite de cartes désordonnées : 

                                    5 - 3 - 6 - 7 - 10 - 9 - 4 - 1 - 2 - 8

Nous choisissons une carte au hasard, par exemple la carte 8. Le but nous l'avons dit : placer celle-ci à sa place définitive en permuttant toutes les cartes de sorte que toutes les cartes inférieures à la carte pivot soient à gauche et celles supérieures à droite. La carte 8 restera donc la carte pivot jusqu'à ce qu'elle prenne sa place.
5 - 3 - 6 - 7 - 10 - 9 - 4 - 1 - 2 - 8
Bon tiens commençons à droite par exemple. On se pose la question suivante : 5 est-il plus grande que 8 ? Si la réponse est non on ne bouge pas la carte si au contraire la réponse est oui, nous échangeons la place de ces deux cartes. La carte 5 ne bougeant pas ici (réponse : NON), donc nous passons à la carte suivante. 
La carte 6 est-elle plus grande que 8 ? Non. On passe à la acarte suivante. La carte 7 est-elle plus grande que 8 ? Non, on passe à la carte suivante. 
La carte 10 est-elle plus grande que la carte 8 ? Oui donc on permutte. 
5 - 3 - 6 - 7 - 8 - 9 - 4 - 1 - 2 - 10
Et on change de sens : la carte, 
3 est-il plus grande que la carte 8 ? Non. on ne bouge pas ici encore.
La carte 9 est-elle plus grande que 8 ? Oui ! Alors on les permutte. 8 prend donc la place de la carte 9. les cartes à gauche ayant été vérifiée, nous allons donc vérifier celle à droite. on commence toujours par la carte la plus à l'extrême de la carte pivot. 
5 - 3 - 8 - 7 - 10 - 9 - 4 - 1 - 2 - 6
Cette fois-ci on se pose la question suivante : 6 est-il plus petit que 8 ? Si oui les deux cartes permuttent autrement elles restent à leur place. Ici c'est donc oui donc on swape ! 
5 - 3 - 6 - 7 - 10 - 9 - 4 - 1 - 2 - 8
Les cartes 5 - 3 - 6  ayant été vérifée, on prend la carte la plus à gauche non vérifé, c'est donc la 7. 
Ayant changé le sens de vérfication on se pause la question inverse : la carte 7 est-elle plus petite que la carte 8 ? Oui ! Pas bouger. 
La carte 10 est-elle plus petite que la carte 8 ? Non ! Donc on swape ! 
5 - 3 - 6 - 7 - 8 - 9 - 4 - 1 - 2 - 10.
Changement de sens : la carte 2 est-elle plus grande la carte 8 ? Non, on change.
5 - 3 - 6 - 7 - 2 - 9 - 4 - 1 - 8 - 10.
Changement de sens : [verification déjà faite des carte 5 - 3 - 6 - 7 - 2, vous suivez toujours ? Donc on commence à la carte la l'extrême de 8 qui est donc 9] la carte 9 est-elle plus petite que la carte 8 ? Non, donc on change.
5 - 3 - 6 - 7 - 2 - 8 - 4 - 1 - 9 - 10.
Changement de sens : la carte la plus à l'extrême = 1. 
La carte 1 est-elle plus grande que la carte 8 ? Non ! 
Hop on swape (?) ! 
5 - 3 - 6 - 7 - 2 - 1 - 4 - 8 - 9 - 10.
Il reste plus que la carte 4 à trier car nous avons à gauche toutes les cartes plus petites que 8 et droite celle plus grande. 
On se pose donc la question : la carte 4 est-elle plus grande que la carte 8 ? La réponse étant non on ne permutte. Les cartes ayant toutes été vérifiées, on peut conclure que la carte 8 à trouver sa place définitive. Elle est donc rangée et c'est donc la dernière carte avec laquelle elle a permuté qui prend la place de la carte pivot, c'est donc ici la carte 4.

Et on recommence les mêmes procédures jusqu'à ce que chaque carte trouve sa place définitive. 



