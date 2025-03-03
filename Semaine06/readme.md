<h1 align="Center">Travail Pratique #2</h1>
<h1 align="Center">🧾 Infologique Inc 🧾</h1>

**Infologique Inc**, une entreprise œuvrant dans la vente de logiciels souhaite créer une application de vente au détail (POS) afin de la proposer à sa clientèle travaillant dans la vente au détail (dont **Atlas Informatique**). Il vous demande de créer une preuve de concept de structure de données permettant la création de reçus d'achat pour une caisse enregistreuse munie d'un lecteur de code à barre. Comme **Infologique Inc** est située en France, elle est consciente qu'elle ne pourra pas vous fournir le matériel nécessaire aux tests avec le lecteur de code à barre. Elle désire que vous soyez en mesure de lui envoyer une solution Visual Studio simulant la création de reçus de vente, simulant ainsi de réels achats. **Infologique Inc.** possède la [base de données](./_bin/products.dat) des produits offerts par son client.

> ATTENTION: **Infologique Inc** exige du code 100% en anglais.

## Devis initial - Affichage des produits

#### Liste des demandes

1. Créer la classe `Product` incluant les sections que vous avez vues en classes ainsi qu'une fonction `toString()` qui retourne une version chaîne de caractères du produit.
2. Créer une structure de données de liste chaînée (classe `ProductList`) permettant de regrouper les données des produits disponibles qui contiendra au minimum :
   1. Un attribut `head` qui pointe sur le premier élément qui sera une `struct` nommée `Node` qui, à son tour, contiendra :
      1. Un attribut `data` de type `Product`.
      2. Un attribut `next` de type `Node` initialisé à `nullptr` par défaut.
      3. Un constructeur permettant de créer un nouveau `Node`.
         > On utilise `struct` pour `Node` car les attributs seront par défaut public et cela est convenable car il n'est accessible que par `ProductList`.
      4. Un destructeur pour libérer l'espace mémoire du produit lié sur la Heap.
   2. Une fonction `add(Product)` qui servira à créer un nouveau `Node` sur la Heap.
   3. Une fonction `print()` qui affichera la liste des produits à l'écran.
   4. Une fonction `getCount()` qui retournera le nombre de produits à l'écran.
   5. Un destructeur pour libérer l'espace mémoire des `Node` présents sur la Heap.
3. Créer une fonction `readProducts(ProductList)` de lecture des produits depuis le fichier `products.dat` :
   1. Lire l'ensemble des données d'un produit dans des variables distinctes.
   2. Créer un nouveau produit sur la `Heap` en utilisant son constructeur.
   3. Ajouter le nouveau produit dans `ProductList`.
4. Effectuer l'affichage des produits à l'écran contenant :
   1. Un entête au nom du client final qui affichera le nombre de produits total provenant de `ProductList`.
   2. La liste de tout les produits disponibles.

<hr/>
<p align="Center"><img src="./images/end.png" alt="drawing" width="150"/></p>
