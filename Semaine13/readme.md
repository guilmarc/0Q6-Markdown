<h1 align="center">Exercices 04</h1>
<h1 align="center">📍 Les Maps 📍</h1>

## Mise en situation

Vous êtes maintenant apte à créer et à utiliser de nombreux types de structures de données, dont les _maps_. Il s'agit d'une structure de données de type clé‑valeur où il est impossible d'enregistrer deux fois une valeur ayant la même clé. C'est très utile, par exemple, lorsqu'on souhaite stocker des produits avec un SKU unique. Si l'utilisateur tente d'entrer une valeur avec une clé existante, l'application écrasera automatiquement la valeur précédente.

## 📚 Question 1 – Map statique typée

En utilisant des tableaux standards comme structure de base et en considérant le code du `main` ci‑dessous, programmez une structure de données nommée `StaticTypedMap` permettant d'enregistrer en mémoire des [produits](./_bin/products.dat) possédant un SKU (`string`) comme **clé** et une description (`string`) comme **valeur**.

Repensez à ce qui a été vu en classe dans les derniers cours afin de résoudre ce problème.

```cpp
class StaticStringMap {
    string keys[MAX_SIZE];
    string values[MAX_SIZE];
    // Votre code ici
};
```

```cpp
void loadProducts(StaticStringMap& products) {
    ifstream file(PRODUCTS_FILE);
    if (!file.is_open()) {
        cout << "Impossible d'ouvrir le fichier " << PRODUCTS_FILE << endl;
        return;
    }

    string code;
    string description;
    string trash;
    while (!file.eof()) {
        getline(file, code, ',');
        getline(file, trash, ',');
        getline(file, trash, ',');
        getline(file, description, ',');
        getline(file, trash);

        products[code] = description;
    }
    file.close();
}

void question01() {
    StaticStringMap products;
    loadProducts(products);
    cout << products;

    // Exemple d'accès à un produit
    string code = "284162";
    cout << endl << "Produit avec le code " << code << " : " << products[code] << endl;
}
```

```plaintext
284162:Un choix parfait pour les gamers recherchant fluidité et rapidité.
602855:Optimisé pour une productivité accrue grâce à des fonctionnalités avancées.
182945:Un produit polyvalent, adapté aux professionnels comme aux particuliers.
573207:Offre une qualité d'image et un confort visuel exceptionnels.
// ...

Produit avec le code 284162 : Un choix parfait pour les gamers recherchant fluidité et rapidité.
```

<hr/>
<p align="center"><img src="./images/end.png" alt="drawing" width="150"/></p>
