<h1 align="Center">Exercices 02</h1>
<h3 align="Center">0Q6 - Structures de données</h3>

## Question 01 - Trance Position

Transposer une matrice carrée 3x3 remplie de chiffres trouvés au hazard. La transposition consiste à inverser les lignes et les colonnes.

```plaintext
Matrice originale :
1 2 3
4 5 6
7 8 9

Matrice transposee :
1 4 7
2 5 8
3 6 9
```

## Question 02 - Multiply

[Multiplier deux matrices](https://www.alloprof.qc.ca/fr/eleves/bv/mathematiques/les-operations-sur-les-matrices-m1467) de 10x10 de chiffres générés au hasard et afficher le résultat à l'écran.

```plaintext
Matrice 1 :
2       1       8       8       1       9       7       3       9       8
0       5       5       9       2       5       2       7       6       0
3       4       9       6       6       1       6       0       5       9
9       9       6       2       6       1       1       9       3       4
9       7       5       4       1       5       1       2       1       5
2       1       8       7       8       7       3       3       0       7
4       4       1       2       5       3       6       1       5       5
1       2       1       9       1       9       2       0       6       3
1       6       9       9       1       7       7       2       7       9
7       9       0       2       3       0       7       2       3       6

Matrice 2 :
5       2       3       9       4       4       9       6       3       3
5       4       3       8       2       5       6       5       1       5
9       7       7       8       7       6       0       0       0       0
2       1       5       1       4       5       2       7       4       9
4       6       5       8       9       6       2       3       2       3
0       7       4       9       3       7       2       2       8       4
2       9       2       2       3       5       5       1       8       0
1       8       5       7       7       3       7       1       0       9
5       8       0       8       2       2       0       4       8       4
3       1       8       6       1       7       6       9       6       7

Produit des matrices :
193     308     239     342     202     288     164     212     289     241
137     233     164     251     181     190     121     137     149     219
216     237     232     300     201     262     161     207     199     188
210     250     219     373     237     236     245     191     120     233
161     164     180     288     149     210     192     182     138     178
163     226     245     293     224     266     146     173     173     202
126     191     135     234     133     181     147     151     176     141
89      164     130     201     108     177     87      153     197     178
216     297     258     347     203     306     182     234     269     254
145     179     145     249     128     190     212     185     160     165
```

## Question03 - Connect 4

<p align="Center"><img src="https://m.media-amazon.com/images/I/71fbNZ8yPXL._AC_SL1500_.jpg" alt="drawing" width="150"/></p>

Simuler un jeu de jeton carré avec **36 cases** de taille identiques. Il y aura deux joueurs :

1. Gaetan Bontemps (le positif en blanc).
2. Babe Boune Darkness (le négatif en noir).

Il jouerons à tour de rôle et sélectionneront où placer leur jeton sur le carton (aléatoirement) de jeu jusqu'à-ce que toutes les cases soient remplis.
Afficher le résultat du carton de jeu comme suit :

```plaintext
B B B B B N
N N N B N B
N B B N N N
B N N N B B
B B N N B N
B N B N B N
```

## DEFI - Question04 - Connect 4 Reloaded

Reprendre **Connect 4** et lui ajouter un algorithme permettant de trouver un gagnant en cours de jeu. Un joueur gagnera s'il réussis à créer une ligne de 4 jeton de sa couleur soit verticalement, soit horizontalement.

```plaintext
Nous avons un gagnant : Gaetan Bontemps en 12 coups !
```

## DÉFI - Question 05 - Connect 4 ReReLoaded

Ajouter la détection de gagnant avec des diagonales de 5 jeton de la même couleur en ligne.

```plaintext
Nous avons un gagnant : Babe Boune Darkness en 15 coups !
```

<p align="Center"><img src="./images/end.png" alt="drawing" width="150"/></p>
