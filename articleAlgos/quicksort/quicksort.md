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
- Il existe de nombreuses versions de quickSort et qui sélectionnent pivot de différentes manières.




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



_________________________________________________________________________________

## en pratique, voici un exemple : 


Prenons une suite de cartes désordonnée : 

                                    5 - 3 - 6 - 7 - 10 - 9 - 4 - 1 - 2 - 8

Nous choisissons une carte au hasard, par exemple la carte 8. Le but nous l'avons dit : placer celle-ci à sa place définitive en permuttant toutes les cartes de sorte que toutes les cartes inférieures à la carte pivot soient à gauche et celles supérieures à droite. 
La __carte 8__ restera donc la carte __pivot jusqu'à ce qu'elle prenne sa place.__

                                    5 - 3 - 6 - 7 - 10 - 9 - 4 - 1 - 2 - __8__

Bon tiens commençons à droite par exemple. On compare avec la carte la plus à l'extrême de 8, qui est la carte 5 et on se pose la question suivante : __la carte 5 est-elle plus grande que 8 ?__ Si la réponse est non on ne bouge pas la carte, si au contraire la réponse est oui, nous échangeons la place de ces deux cartes. La carte 5 ne bougeant pas ici (réponse : __NON__), donc nous passons à la carte suivante. 

                                    [[5]]- 3 - 6 - 7 - 10 - 9 - 4 - 1 - 2 - __8__

On passe à la carte suivante, la plus à l'extrême de 8 : __la carte 3 est-elle la plus grande ? __NON__ donc on ne la déplace pas, elle reste à sa place et on passe à la carte suivante (on oublie pas, toujours la plus à l'extrême de la carte pivot et non vérifée). 
                                    [5]- [[3]]- 6 - 7 - 10 - 9 - 4 - 1 - 2 - __8__

__La carte 6 est-elle plus grande que la carte 8 ? __NON__ ! Alors pas de changement, elle reste à sa place.Et on passe à la suivante.

                                    [5-3] - [[6]] - 7 - 10 - 9 - 4 - 1 - 2 - __8__

__La carte 7 est-elle plus grande que la carte 8 ? __NON__ ! 

                                    [5-3-6] - [[7]] - 10 - 9 - 4 - 1 - 2 - __8__
                                    
__La carte 10 est-elle plus grande que la carte 8 ?__ Oui donc on permutte. 

                                    [5-3-6-7] - [[10]] - 9 - 4 - 1 - 2 - __8__

                                    [5 - 3 - 6 - 7]- __8__- 9 - 4 - 1 - 2 - [10]


Et on change de sens : __la carte, 2 est-elle plus petite que que la carte 8 ?__ Oui donc swape et on passe à la question suivante ! 

                                    [5 - 3 - 6 - 7]- __8__- 9 - 4 - 1 - [[2]] - [10]
                                    [5 - 3 - 6 - 7- 2 - 1] __8__ - 4 - 1 - [9 - 10]

__La carte 1 est-il plus petite que la carte 8 ? Oui.__ on change les places. Et changement de sens...

                                    [5 - 3 - 6 - 7]- __8__- 9 - 4 - [[1]] - [2 - 10]
                                    [5 - 3 - 6 - 7- 2 - 1] - 4 - __8__ - [2 - 10]

__La carte 9 est-elle plus grande que la carte 8 ? Oui !__ Alors on les permutte. 8 prend donc la place de la carte 9. Hop swape ! 

                                    [5 - 3 - 6 - 7- 1]- [[9]]- 4 - __8__ - [2 - 10]
                                    [5 - 3 - 6 - 7- 1]- 8 - 4 -  [9 - 2 - 10]


Il reste plus que la carte 4 à trier car nous avons à gauche toutes les cartes plus petites que 8 et droite celle plus grande. 
On se pose donc la question : la carte 4 est-elle plus grande que la carte 8 ? La réponse étant non on ne permutte. Les cartes ayant toutes été vérifiées, on peut conclure que la carte 8 à trouver sa place définitive. Elle est donc rangée et c'est donc la dernière carte avec laquelle elle a permuté qui prend la place de la carte pivot, c'est donc ici __la carte 4.__

                                    [5 - 3 - 6 - 7- 1 - ]- __8__- [[4]]- [9 - 10]
                                    [5 - 3 - 6 - 7- 1 - 4]- __8__- [9 - 10]
                                    5 - 3 - 6 - 7- 1 - __4__ [8]- 9 - 10

Et on recommence les mêmes procédures jusqu'à ce que chaque carte trouve sa place définitive. 

En espérant que cette algo n'est plus un casse-tête pour vous.


>>>>>>> 
