# Tri par Bulles 

Tout d'abord, commençons par le commencement. Imaginons que nous ayons huits cartes, allant de 1 à 8. Ces cartes sont positionnés de façon aléatoire dans un tableau.

![](cartes.png)

Nous avons 8 cartes mais nous allons commencer par l'index 0. Ainsi, dans cet exemple, nous ne dirons pas "carte 6" mais plutôt "index 0". Nous aurons donc 7 index.

Il faut savoir que l'index 0 peut se trouver aussi bien à gauche qu'à droite. Tout dépend où vous souhaitez démarrer. Dans cet exemple, cependant, l'ordre de lecture sera de gauche à droite.

![](ordre.png)

Il as plusieurs choses à savoir :

* Il faut toujours comparer deux valeurs entre elles.
* Comme nous commençons par la gauche, il faudra comparer avec la valeur à gauche.
* Il faut se poser cette question : **Est-ce que l'index X est-il supérieur à l'index Y ?**
* Deux choix s'offrent alors à nous. Si la réponse est **"oui"**, nous devons changer de placer les deux index. NOus continuerons alors notre lancée. Si cependant, la réponse est **"non"**, les index restent à la même place et on _"next"_. On passe à l'autre index.

![](index.png)