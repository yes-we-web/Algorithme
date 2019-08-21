# Tri par selection (selection sort) :

## Présentation du Tri par selection : 

Le principe du tri par sélection est d'aller chercher le plus petit élément du tableau pour le mettre en premier.

(il sera l'index 0) puis, partir de l'index 1 (la seconde données du tableau) continuer sur sa droite et aller chercher l'élément plus petit que lui.  
On compare toujours en ce demandant : "est-ce que l'index de gauche et plus petit que l'index de droite ?"

(on remplace bien sur les mots gauche et droite par le numéro de l'index) 
par exemple : "est-ce que l'index 1 est plus petit que l'index 2 ?".

Si jamais c'est le cas, on compare l'index 1 avec l'index 3, une fois que l'on a trouver un élément plus petit que l'index 1
on compare cette élément avec le reste du tableau.

Si par exemple l'index 4 est plus petit que l'index 1 on prend l'index 4 comme point de comparaison et on continue dans le tableau jusqu'à trouver un élément plus petit que l'index 4.

Une fois que l'on à fini de comparer tout le tableau on a l'élément le + petit, on swap donc sa place avec l'index 1.

Pour la suite c'est la même chose, on reprend à partir de l'index 2 et on le compare avec les autres index pour trouver un éléments 
plus petit que lui.
 
Une fois que l'on a trouvé cette élément on prend l'élément plus petit que l'index 2 et on le compare avec 
le reste du tableau pour trouver un élément encore plus petit.

On fait ça jusqu'a la fin du tableau et on se retrouve avec un nombre 
plus grand que l'index 0 et 1 mais plus petit que le reste du tableau on le place donc en index 2. 

Pour finir cette Algorithme c'est très simple, il suffit 
juste de continuer à faire la même chose en prenant maintenant l'index 3 comme point de départ.

un exemple du Tri par selection avec un gif : ![](images/Selection-Sort.gif)
