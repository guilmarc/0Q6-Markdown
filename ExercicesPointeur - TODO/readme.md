<h1 align="center">Exercices Supplémentaires</h1>
<h1 align="center">Les pointeurs</h1>

## 📚 Question 1 - Swap

Écrire une fonction swap qui a comme paramètres deux pointeurs vers des entiers et qui échange le contenu des deux entiers pointés. Tester cette fonction en écrivant un programme qui échange le contenu de deux entiers a et b en appelant cette fonction.

## 🙃 Question 2 - Le monde à l'envers

En utilisant la pile créée en Question 1, créer un algorithme qui demande une chaîne de caractères à l'utilisateur et qui affiche ensuite cette chaîne inversée.

```plaintext
Entrez votre phrase : J'aime utiliser la pile!
Alors vous dites : !elip al resilitu emia'J
```

## ✔️ Question 3 - Prettier Light

Vous connaissez maintenant **Prettier**, un formateur de code dans Visual Studio Code. Dans cette question, vous devez utiliser la pile afin de valider si les codes suivants contiennent un nombre équilibré d'accolades ouvrantes et fermantes. Copiez les codes dans des variables `code1`, `code2` et `code3` en ajoutant un `R` au début et des paranthèses `()` alentour du code afin d'être en mesure d'écrire sur plusieurs lignes.

```cpp
string code1 = R"(if(age >= 18) {...)"
```

#### Code #1

```cpp
if(age >= 18) {
   if(hasExperience) {
      cout << "Oui vous pouvez travailler dans ma micro-brasserie !";
   }
}
```

```plaintext
Ce code est équilibré !
```

#### Code #2

```cpp
if(age >= 18) {
   if(!hasExperience) {
      cout << "Je suis désolé, je cherche quelqu'un avec expérience !"
   }}
}
```

```plaintext
Il y a trop d'accolades fermantes !
```

#### Code #3

```cpp
if(age >= 18) {
   if(hasExperience) {
      {cout << "Oui vous pouvez travailler dans ma micro-brasserie !"
   }
}
```

```plaintext
Il y a trop d'accolades ouvrantes !
```

## DÉFI ✔️ Question 4 - Prettier SemiLight
Reprenez la solution Prettier Light et affichez le numéro de ligne lorsqu’une erreur de balancement des accolades est détectée :

#### Code #2

```cpp
if(age >= 18) {
   if(!hasExperience) {
      cout << "Je suis désolé, je cherche quelqu'un avec expérience !"
   }}
}
```

```plaintext
Il y a trop d'accolades fermantes à la ligne #4 !
```

<hr/>
<p align="center"><img src="./images/end.png" alt="drawing" width="150"/></p>
