# HEAPSORT ( le tri par tas)

Le tri par tas (Heapsort) est un algorithme de tri très performant même s’il n'est en moyenne deux fois plus lent que le tri rapide.
On peut définir deux sortes de tas binaires : les tas min et les tas max.
* Tas-Min : chaque élément est supérieur à son parent.
* Tas-Max : chaque élément est inférieur à son parent.
Le tas [les valeurs] peut être représenté comme un arbre binaire, il peut être stocké de façon très simple dans un tableau. Le premier élément est la racine, le deuxième et le troisième sont les deux descendants du premier élément. Le premier élément dit (parent), le deuxième dit (enfant de gauche), et le troisième dit (enfant de droite), toujours procède de gauche vers la droite en descendant par ligne. 

### Exemple

![Exemple en image](http://sdz.tdct.org/sdz/medias/uploads.siteduzero.com_files_286001_287000_286613.jpg)


Continué le processus pour que tous les valeurs soient présents dans l'arbre, puis deviennent des indices de comparaisons.
les indices se comparent de deux manières différentes soit par Tas-Min le principe est de classer les indices par ordre croissant ou par Tas-Max à l'inverse classement décroissant.

### nous allons procéder par Tas-Max ;

Pour commencer comparer le premier parent (gauche) de l'avant-dernière ligne avec son premier enfant (gauche) de la dernière ligne, le plus grand des deux devient parent et l'autre enfant (gauche).
Ensuite compare le nouveau parent avec le deuxième enfant (droite), le plus grand des deux remontes et devient parent. 
puis faite le même processus pour le parent et enfants de droit s'il y a.
Une fois les dernières lignes faite, refaire le processus avec les nouveaux parents et ses enfants des autres lignes en remontent de gauche à droite et ainsi de suite pour que le plus grand nombre soit à la tête de l'arbre (parente racine).

Le plus grand nombre est en tête de l'arbre, on peut le retire et dire qu'il est classé, le dernier nombre du bas à droite de l'arbre devient parent a la racine, et on recommence le processus complet, du bas vers le haut et de gauche vers la droite pour que le deuxième plus grand nombre remonte a la tête de l'arbre pour qu'ensuite il se classe et que l'on re-recommence le processus.
À la fin tous les nombres seront classes du plus grand aux plus petits dans votre tableau


### Exemple : Tas-Max
![Exemple de tas-max](https://upload.wikimedia.org/wikipedia/commons/f/fe/Heap_sort_example.gif)



Source : [Wikipédia](https://fr.wikipedia.org/wiki/Tri_par_tas) - 
         [Turoriel](http://sdz.tdct.org/sdz/le-tri-par-tas.html)














 