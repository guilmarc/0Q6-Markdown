<h1 align="Center">Travail Pratique #1</h1>
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
7. Utiliser des attributs et méthodes **statiques** pour stocker le nombre d'étoiles et de planètes créées et l'afficher à la fin du listing des planètes.

> ATTENTION: Les fonctions de lecture depuis un fichier devront être adaptées car il est interdit d'utiliser des variables de paramétrage comme NOMBRE_PLANETES ou NOMBRE_ETOILES. Vous devez déduire le nombre de planètes et d'étoiles selon le nombre qu'il y a dans les fichiers de données.

> ATTENTION: **Intergalactik** n'aime pas les tableaux standards, il vous demandent d'utiliser les `vector` sans même être en mesure de vous expliquer comment. Vous devrez faire preuve d'autonomie!

> ATTENTION: **Intergalactik** exige du code 100% en anglais.

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
| Mercure       |          4879 |      60812199253 |
| Vénus         |         12103 |     928276498359 |
| Terre         |         12756 |    1086780374578 |
| Mars          |          6779 |     163115472020 |
| Jupiter       |        139820 | 1431219183979161 |
| Saturne       |        116460 |  827043995236586 |
| Uranus        |         50724 |   68334297976022 |
| Neptune       |         49244 |   62525651174218 |
----------------------------------------------------

TRAPPIST-1
----------------------------------------------------
| PLANETE       | DIAMETRE (km) | VOLUME (km3)     |
----------------------------------------------------
| TRAPPIST-1b   |         11600 |     817282544106 |
| TRAPPIST-1c   |         11400 |     775733969159 |
| TRAPPIST-1d   |          8000 |     268082346666 |
| TRAPPIST-1e   |          9100 |     394568519648 |
| TRAPPIST-1f   |         10400 |     588976915626 |
| TRAPPIST-1g   |         10800 |     659583103679 |
| TRAPPIST-1h   |          9300 |     421159984604 |
----------------------------------------------------

Luyten's Star
----------------------------------------------------
| PLANETE       | DIAMETRE (km) | VOLUME (km3)     |
----------------------------------------------------
| GJ 273b       |         14000 |    1436753826666 |
| GJ 273c       |         12000 |     904777919999 |
| GJ 273d       |         11500 |     796327615208 |
| GJ 273e       |         10500 |     606130520624 |
----------------------------------------------------

Gliese 581
----------------------------------------------------
| PLANETE       | DIAMETRE (km) | VOLUME (km3)     |
----------------------------------------------------
| Gliese 581b   |         23000 |    6370620921666 |
| Gliese 581c   |         15500 |    1949814743541 |
| Gliese 581d   |         21000 |    4849044164999 |
| Gliese 581e   |         12000 |     904777919999 |
----------------------------------------------------

Gliese 667 C
----------------------------------------------------
| PLANETE       | DIAMETRE (km) | VOLUME (km3)     |
----------------------------------------------------
| Gliese 667Cb  |         14000 |    1436753826666 |
| Gliese 667Cc  |         12000 |     904777919999 |
| Gliese 667Cd  |         12500 |    1022652994791 |
| Gliese 667Ce  |         11500 |     796327615208 |
| Gliese 667Cf  |         10700 |     641430473061 |
| Gliese 667Cg  |          9800 |     492806562546 |
----------------------------------------------------

Nombre de planètes créées : 29
Nombre d'étoiles créées : 5
```

<p align="Center"><img src="./images/end.png" alt="drawing" width="150"/></p>
