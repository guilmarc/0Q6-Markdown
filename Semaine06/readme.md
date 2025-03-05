<h1 align="Center">Travail Pratique #2</h1>
<h1 align="Center">🧾 Infologique Inc. 🧾</h1>

**Infologique Inc.**, une entreprise œuvrant dans la vente de logiciels, souhaite créer une application de vente au détail (POS) afin de la proposer à sa clientèle travaillant dans la vente au détail (dont **Atlas Informatique**). Il vous demande de créer une preuve de concept de structure de données permettant la création de reçus d'achat pour une caisse enregistreuse munie d'un lecteur de code-barres. Comme **Infologique Inc.** est située en France, elle est consciente qu'elle ne pourra pas vous fournir le matériel nécessaire aux tests avec le lecteur de code-barres. Elle désire que vous soyez en mesure de lui envoyer une solution Visual Studio capable de simuler la création de reçus de vente et de reproduire de réels achats. **Infologique Inc.** possède la [base de données](./_bin/products.dat) des produits offerts par son client.

> ATTENTION: **Infologique Inc.** exige du code 100% en anglais.

## Devis #1 - Affichage des produits

1. Créer la classe `Product` incluant les sections que vous avez vues en classe ainsi qu'une fonction `toString()` qui retourne une version chaîne de caractères du produit.
2. Créer une structure de données de liste chaînée (classe `ProductList`) permettant de regrouper les données des produits disponibles qui contiendra au minimum :
   1. Un attribut `head` qui pointe sur le premier élément qui sera une `struct` nommée `Node` qui, à son tour, contiendra :
      1. Un attribut `data` de type `Product`.
      2. Un attribut `next` de type `Node` initialisé à `nullptr` par défaut.
      3. Un constructeur permettant de créer un nouveau `Node`.
         > On utilise `struct` pour `Node` car les attributs seront par défaut public et cela est convenable car il n'est accessible que par `ProductList`.
   2. Une fonction `add(Product)` qui servira à créer un nouveau `Node` sur la Heap.
   3. Une fonction `print()` qui affichera la liste des produits à l'écran.
   4. Une fonction `getCount()` qui retournera le nombre total de produits à l'écran.
   5. Un destructeur pour libérer l'espace mémoire des `Node` aloué sur la Heap.
3. Créer une fonction `readProducts(ProductList)` de lecture des produits depuis le fichier `products.dat` :
   1. Lire l'ensemble des données d'un produit dans des variables distinctes.
   2. Créer un nouveau produit en utilisant son constructeur.
   3. Ajouter le nouveau produit dans une nouvelle `Node` de `ProductList` en assignant le produits à `data`.
4. Effectuer l'affichage des produits à l'écran contenant :
   1. Une entête au nom du client final qui affichera le nombre de produits total provenant de `ProductList`.
   2. La liste de tous les produits disponibles.

## Devis #2 - Impression des coupons de caisse

Afin de pouvoir utiliser la liste chaînée dans plusieurs projets, **Infologique Inc** vous demande maintenant de transformer `ProductList` en une structure de données de liste chaînée générique nommée `LinkedList`. Vous serez, par la suite, en mesure de faire générer les coupons de caisse aléatoirement :

1. Transformer la solution précédente en utilisant `LinkedList`.
   1. Ajouter une méthode `dataAt(index)` retournant la donnée de la liste à l'index entré en paramètre.
   2. Ajouter une méthode `getFirst()` qui retourne le premier `data` de la liste ou `null` si la liste est vide.
   3. Ajouter une méthode `next()` qui retourne le prochain `data` de la liste ou `null` si aucun élément suivant.
2. Créez une classe `Sale` contenant une liste de produits achetés `items` de type `LinkedList` ainsi que les méthodes nécessaires.
3. Ajoutez entre 3 à 10 produits sélectionnés au hasard dans la liste des produits avec une quantité achetée de 1 à 5, aussi au hasard.
   > Ne pas se soucier pour l'instant du cas où le hasard sélectionne plus d'une fois le même produit. Nous gérerons ce cas d'utilisation plus tard.
4. Créer un coupon de caisse représentant la vente effectuée.
5. Recréer un nouveau coupon (pas besoin de sauvegarder les coupons précédents) quand on appuie sur `Espace` et quitter sur `Esc`.
   > Lire la liste des produits qu'une seule fois.

### Visuel du coupon de caisse désiré

```
-----------------------------
|      Infologique Inc      |
-----------------------------
|      2025-03-01 16h35     |
-----------------------------
| 002 Western Digital       |
|     WD Black SN850 1To    |
|     2065.12       4130.20 |
|                           |
| 005 Nvidia                |
|     GeForce RTX 4070      |
|      138.46        692.30 |
|                           |
|     TOTAL:        4822.54 |
-----------------------------
```

<hr/>
<p align="Center"><img src="./images/end.png" alt="drawing" width="150"/></p>
