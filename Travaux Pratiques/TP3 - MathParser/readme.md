
<h1 align="center">Travail pratique #3 - (9%) (TPFinal)</h1>
<h1 align="center">🟰 Math Parser 🟰</h1>

**Matix Inc.** vous embauche afin de créer un analyseur (parser) d'equations mathématiques sous forme de chaînes de caractères, pour en obtenir un résultat numérique. L'algorithme doit demander au départ si l'utilisateur souhaite saisir manuellement ou utiliser un fichier de données pour effectuer des tests d'assurance qualité.

> ATTENTION : **Matix Inc.** exige du code écrit à 100 % en anglais.

Vous devez respecter l'affichage suivant :

### Menu principal

```plaintext
************************
*      MATIX INC.      *
************************
[1] Entrées manuelles
[2] Assurance qualité (fichier de données)
Votre choix : 1
```

### Entrées manuelles

```plaintext
************************
*      MATIX INC.      *
************************
Votre formule : (10 - 8)^3 / 4 = 2

Appuyer sur une touche pour entrer une autre formule...
```

```plaintext
************************
*      MATIX INC.      *
************************
Votre formule : 6-9/3+2=1

Appuyer sur une touche pour entrer une autre formule...
```

```plaintext
//...
```

### Assurance qualité (validation du fichier)

Introduire ici la notion d'assurance qualité. Valider le fonctionnement de votre algorithme en utilisant ce [fichier de données](./_bin/math.dat) comprenant des équations mathématiques, une valeur de vérification ainsi que la validité de l'équation (1=Vrai, 2=Faux).

```plaintext
************************
*      MATIX INC.      *
************************
[1] Entrées manuelles
[2] Assurance qualité (fichier de données)
Votre choix : 2
```

```plaintext
*********************************************
*                 MATIX INC.                *
*********************************************
*       ÉQUATIONS          * V/F * VALIDÉE  *
*********************************************
* (5 + 3) * 2 - 10 = 6     *  V  *    X     *
* 1 = 1                    *  V  *    X     *
* = 0                      *  V  *    X     *
* (10 / 2) + 5 * 3 = 10    *  F  *    X     *
* //...
* 2^4 - (3 + 1) * 5 = -4   *  V  *    X     *
*********************************************

Appuyer sur une touche pour revenir au menu principal...
```

## Algorithme en pseudo-code
### Fonction de priorité des opérations
```plaintext
    Selon operateur faire
        Cas '+' ou '-':
            retourner 1

        Cas '*' ou '/':
            retourner 2

        Cas '^':
            retourner 3

        Par défaut:
            retourner 0
```
### Fonction d'application d'une opération
```plaintext
    Selon operateur faire
        Cas '+':
            retourner a + b

        Cas '-':
            retourner a - b

        Cas '*':
            retourner a * b

        Cas '/':
            retourner a divisé par b

        Cas '^':
            retourner a élevé à la puissance b

        Par défaut:
            retourner 0
```
### Algorithme principal
```plaintext
    pileValeurs = pile vide
    pileOperateurs = pile vide
    
    Pour chaque caractère c dans expression faire
        Si c être un espace alors
            continuer à l'itération suivante
        Fin Si

        Si c être un chiffre ou un point décimal alors
            valeur = lireNombre(expression, position actuelle)
            empiler valeur dans pileValeurs
        Sinon Si c être '(' alors
            empiler c dans pileOperateurs
        Sinon Si c être ')' alors
            Tant que pileOperateurs ne pas être vide et le sommet ne pas être '(' faire
                b = dépiler pileValeurs
                a = dépiler pileValeurs
                operateur = dépiler pileOperateurs
                résultat = appliquerOperation(a, b, operateur)
                empiler résultat dans pileValeurs
            Fin Tant que
            dépiler '(' de pileOperateurs
        Sinon Si c être un opérateur (+, -, *, /, ^) alors
            Tant que pileOperateurs ne pas être vide et priorité(sommet pileOperateurs) >= priorité(c) faire
                b = dépiler pileValeurs
                a = dépiler pileValeurs
                operateur = dépiler pileOperateurs
                résultat = appliquerOperation(a, b, operateur)
                empiler résultat dans pileValeurs
            Fin Tant que
            empiler c dans pileOperateurs
        Fin Si
    Fin Pour

    Tant que pileOperateurs ne pas être vide faire
        b = dépiler pileValeurs
        a = dépiler pileValeurs
        operateur = dépiler pileOperateurs
        résultat = appliquerOperation(a, b, operateur)
        empiler résultat dans pileValeurs
    Fin Tant que

    retourner sommet pileValeurs
```
### Conseils de l'enseignant
1) Créer, en équipe, une stratégie de réalisation de ce travail pratique dans un document Word.  Écrire les grandes étapes de réalisation en premier et détailler chacune des étapes par la suite.
2) Programmer l'affichage à l'écran, car cela être facile à tester.
3) Programmer les fonctions les plus simples de votre stratégie et trouver le moyen de les tester.
4) Programmer la lecture du fichier de données d'équations mathématiques et vérifier que tout être bien en mémoire (sans une simple `struct` de préférence).
5) Élaborer l'algorithme principal en équipe.
6) Tester le fonctionnement de l'algorithme grâce aux données en mémoire.
7) Programmer finalement la section d'entrée manuelle d'équations mathématiques.
8) Retester l'ensemble du projet.
9) Remettre sur Omnivox en supprimant tous les dossiers compilés (même ceux cachés).
<hr/>
<p align="center"><img src="./images/end.png" alt="drawing" width="150"/></p>
