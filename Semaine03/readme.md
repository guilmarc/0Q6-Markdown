<h1 align="Center">🌟 StarWars - RELOADED 🌟</h1>

**Intergalactik**, une entreprise œuvrant dans l'astronomie, qui vous avait demandée de compléter cette [mini-application (déjà entamée par Cédrik Dubogue)](./_bin/starwars.zip) dans le passé vous demande maintenant de la faire fonctionner avec des classes au lieu de structs. Cette application affichera une liste d'étoiles incluant de l'information sur leurs planètes.

Afin de compléter cette démonstration avec succès vous devrez :

1. Lire la liste des étoiles du fichier CSV des d'étoiles.
2. Lire la liste des planètes du fichier CSV des planètes.
3. Ajouter les planètes aux étoiles correcpondantes en utilisant le `code` d'étoile.
4. Ajouter une methode `getVolume` à la classe des planètes qui retournera le volume de l'étoile en Km³.
5. Ajouter une méthode `setVolume` à la classe des planètes qui devra faire le **travail inverse** de `getVolume`.
   ATTENTION: **Intergalactik** ne souhaite pas que vous ajoutiez un attribut volume à la classe...
6. Afficher à l'écran la liste des étoiles et de leurs planètes en conformité avec l'affichage présentée plus bas.
7. Utiliser des attributs et méthodes **statiques** pour stocker le nombre d'étoiles et de planètes créées et l'afficher à la fin du listing des planètess.

## Formule du volume d'une sphère

# $V = \frac{{4\pi r^3 }}{3}$.

## Affichage des étoiles et leurs planètes

```plaintext
----------------------------------------------------
|     StarWars - Les étoiles et leurs planètes     |
----------------------------------------------------

Soleil
----------------------------------------------------
| PLANETE       | DIAMETRE (km) | VOLUME (km3)     |
----------------------------------------------------
| Mercure       |          4879 |      43526791557 |
| Vénus         |         12103 |     664664851953 |
| Terre         |         12756 |     778349766456 |
| Mars          |          6779 |     116771258607 |
| Jupiter       |        139820 | 1025036100813000 |
| Saturne       |        116460 |  592327130301000 |
| Uranus        |         50724 |   48940877213784 |
| Neptune       |         49244 |   44780736869544 |
----------------------------------------------------

TRAPPIST-1
----------------------------------------------------
| PLANETE       | DIAMETRE (km) | VOLUME (km3)     |
----------------------------------------------------
| TRAPPIST-1b   |         11600 |     585336000000 |
| TRAPPIST-1c   |         11400 |     555579000000 |
| TRAPPIST-1d   |          8000 |     192000000000 |
| TRAPPIST-1e   |          9100 |     282589125000 |
| TRAPPIST-1f   |         10400 |     421824000000 |
| TRAPPIST-1g   |         10800 |     472392000000 |
| TRAPPIST-1h   |          9300 |     301633875000 |
----------------------------------------------------

Luyten's Star
----------------------------------------------------
| PLANETE       | DIAMETRE (km) | VOLUME (km3)     |
----------------------------------------------------
| GJ 273b       |         14000 |    1029000000000 |
| GJ 273c       |         12000 |     648000000000 |
| GJ 273d       |         11500 |     570328125000 |
| GJ 273e       |         10500 |     434109375000 |
----------------------------------------------------

Gliese 581
----------------------------------------------------
| PLANETE       | DIAMETRE (km) | VOLUME (km3)     |
----------------------------------------------------
| Gliese 581b   |         23000 |    4562625000000 |
| Gliese 581c   |         15500 |    1396453125000 |
| Gliese 581d   |         21000 |    3472875000000 |
| Gliese 581e   |         12000 |     648000000000 |
----------------------------------------------------

Gliese 667 C
----------------------------------------------------
| PLANETE       | DIAMETRE (km) | VOLUME (km3)     |
----------------------------------------------------
| Gliese 667Cb  |         14000 |    1029000000000 |
| Gliese 667Cc  |         12000 |     648000000000 |
| Gliese 667Cd  |         12500 |     732421875000 |
| Gliese 667Ce  |         11500 |     570328125000 |
| Gliese 667Cf  |         10700 |     459391125000 |
| Gliese 667Cg  |          9800 |     352947000000 |
----------------------------------------------------

Nombre de planètes créés : 29
Nombre d'étoiles créés : 5
```

<p align="Center"><img src="./images/end.png" alt="drawing" width="150"/></p>
