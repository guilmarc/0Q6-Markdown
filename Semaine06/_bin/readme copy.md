<h1 align="Center">Travail Pratique #2</h1>
<h1 align="Center">Infologique Inc</h1>

**Infologique Inc**, une entreprise œuvrant dans la vente de logiciels souhaite créer une application de vente au détail (POS) afin de la proposer à sa clientèle oevrant dans la vente au détail, dont **Atlas Informatique**.  Il vous demande de créer une preuve de concept de structure de données permettant la création de reçu d'achat pour une caisse enregistreuse munie d'un lecteur de code à barre.  Comme **Infologique Inc** est située en France, elle est consciente qu'elle ne pourra pas vous fournir le matériel nécessaire aux tests avec le lecteur de code à barre.  Elle désire que vous soyez en mesure de lui envoyer une solution Visual Studio simulant la création de reçu de vente, simulant ainsi de réels achats.  **Infologique Inc.** possède la base de donnée des produits offerts par son client.

> ATTENTION: **Infologique Inc** exige du code 100% en anglais.

Elle a divisé le projet en 3 devis distincts :

## Devis #1
### Liste des demandes
1. Créer une liste chaînée (classe ProductList) permettant de structurer les données des produits disponibles.
2. Permettre d'ajouter une option lors de l'instanciation de la liste pour que celle-ci place les produits en ordre croissant ou décroissant de prix.  Si l'option n'est pas entrée, ajouter simplement dans la liste dans l'ordre de la base de données.
> Attention, il n'est pas demandé ici de pouvoir retrier la liste une fois remplie mais seulement de placer les éléments au bon endroit à chaque ajout.  
3. Effectuer l'affichage de l'ensemble des produits provenant de la base de données.
4. Remettre votre solution au devis #1 à **Infologique Inc** afin d'obtenir votre paiement.
### Spécifications

ProduitList devra offrir ces méthodes :

1. add(product) --> Ajoute un élément à selon que l'option de trie sélectionnée (ou pas).
2. addTop(product) --> Ajoute un produit au début de la liste.
3. getProductAt(index) --> Retourne le produit à l'index demandé.
4. removeAt(index) --> Supprime un produit de la liste à l'index demandé.
5. getCount() --> Retourne le nombre de produits présents dans la liste.

#### Visuel d'un reçu de caisse
```
---------------------------
|     Infologique Inc.    |
---------------------------
|     2025-03-01 16h35    |
---------------------------
| 002 Western Digital     |
|     WD Black SN850 1To  |  
|     2065.12     4130.24 |
|                         |
| 005 Nvidia              |
|     GeForce RTX 4070    |
|      138.46      692.30 |
|                         |
|     TOTAL:      4822.54 |
--------------------------- 
```

## Devis #2
En analyse par le client...

<p align="Center"><img src="./images/end.png" alt="drawing" width="150"/></p>
