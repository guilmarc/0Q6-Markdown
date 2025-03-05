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
4. Effectuer l'affichage des produits à l'écran selon le modèle attendu.
### Résultat attendu
```plaintext
-----------------------------------------------------------------
| #SKU    | BRAND           | MODEL                  |   PRICE  |
-----------------------------------------------------------------
| #284162 | Western Digital | WD Black SN850 1To     | 2065.12$ |
| #602855 | Netgear         | Nighthawk AX12         | 1534.69$ |
| #298905 | Brother         | HL-L2350DW             | 1291.80$ |
| #182945 | Logitech        | MX Keys                |  956.09$ |
| #573207 | Dell            | XPS 13                 | 1795.48$ |
| #016246 | Kingston        | Fury Beast 16Go DDR5   |  380.32$ |
| #961569 | Logitech        | MX Keys                |  362.00$ |
| #678382 | Dell            | XPS 13                 |  832.04$ |
| #269706 | Corsair         | K70 RGB Pro            | 1675.58$ |
| #447087 | Razer           | DeathAdder V2          | 1307.86$ |
| #353719 | Logitech        | MX Keys                |  887.90$ |
| #049253 | Logitech        | MX Keys                | 1234.16$ |
| #711218 | Lenovo          | ThinkPad X1 Carbon     |  262.38$ |
| #395563 | Western Digital | WD Black SN850 1To     |  294.37$ |
| #264522 | Acer            | Predator Helios 300    | 2439.24$ |
| #762794 | Western Digital | WD Black SN850 1To     |  660.47$ |
| #541852 | Kingston        | Fury Beast 16Go DDR5   | 1151.94$ |
| #979447 | Dell            | XPS 13                 |  829.25$ |
| #273525 | Samsung         | Odyssey G7 27          | 1760.33$ |
| #992423 | Razer           | DeathAdder V2          |  429.51$ |
| #657273 | Corsair         | K70 RGB Pro            |  396.03$ |
| #983947 | Samsung         | Odyssey G7 27          |  509.30$ |
| #328702 | HP              | Pavilion 15            |  571.65$ |
| #966219 | Samsung         | Odyssey G7 27          |  419.18$ |
| #225363 | Brother         | HL-L2350DW             |  591.91$ |
| #089291 | Dell            | XPS 13                 |  782.16$ |
| #131171 | Western Digital | WD Black SN850 1To     | 1874.69$ |
| #961864 | Kingston        | Fury Beast 16Go DDR5   | 2341.99$ |
| #157950 | Lenovo          | ThinkPad X1 Carbon     |  865.79$ |
| #771443 | Kingston        | Fury Beast 16Go DDR5   | 2446.29$ |
| #343616 | Nvidia          | GeForce RTX 4070       |  138.46$ |
| #056621 | Kingston        | Fury Beast 16Go DDR5   | 1472.27$ |
| #002751 | Lenovo          | ThinkPad X1 Carbon     |  539.35$ |
| #090415 | Kingston        | Fury Beast 16Go DDR5   |  521.16$ |
| #023320 | Kingston        | Fury Beast 16Go DDR5   |  667.01$ |
| #345652 | Dell            | XPS 13                 |  890.99$ |
| #300948 | Asus            | ROG Strix G15          | 1903.61$ |
| #167154 | Razer           | DeathAdder V2          | 1676.51$ |
| #699540 | Brother         | HL-L2350DW             |  945.26$ |
| #233160 | Dell            | XPS 13                 | 2323.92$ |
| #266093 | HP              | Pavilion 15            | 2442.58$ |
| #044816 | Apple           | MacBook Air M2         | 2386.40$ |
| #720968 | Brother         | HL-L2350DW             | 2494.26$ |
| #755702 | Samsung         | Odyssey G7 27          | 2342.28$ |
| #824519 | Dell            | XPS 13                 |  929.38$ |
| #939821 | Samsung         | Odyssey G7 27          | 2466.60$ |
| #898779 | Kingston        | Fury Beast 16Go DDR5   | 1225.49$ |
| #790197 | Logitech        | MX Keys                | 2435.74$ |
| #240463 | Brother         | HL-L2350DW             |  712.31$ |
| #597621 | Samsung         | Odyssey G7 27          |  706.82$ |
| #042334 | Samsung         | Odyssey G7 27          | 1463.47$ |
| #585822 | Netgear         | Nighthawk AX12         | 1925.91$ |
| #290015 | Nvidia          | GeForce RTX 4070       | 1163.31$ |
| #349776 | Apple           | MacBook Air M2         |   59.53$ |
| #069012 | Acer            | Predator Helios 300    | 1119.65$ |
| #726721 | Dell            | XPS 13                 |  235.57$ |
| #043312 | Dell            | XPS 13                 |  722.86$ |
| #964958 | Sony            | WH-1000XM5             | 1962.38$ |
| #164824 | Corsair         | K70 RGB Pro            |  188.40$ |
| #694375 | Acer            | Predator Helios 300    | 2128.34$ |
| #865555 | Logitech        | MX Keys                | 2333.52$ |
| #619288 | Nvidia          | GeForce RTX 4070       | 2131.54$ |
| #544295 | Samsung         | Odyssey G7 27          | 1170.29$ |
| #049756 | Netgear         | Nighthawk AX12         |  850.84$ |
| #532624 | Western Digital | WD Black SN850 1To     | 1861.42$ |
| #207878 | Corsair         | K70 RGB Pro            |  988.98$ |
| #135111 | Razer           | DeathAdder V2          | 1691.30$ |
| #873767 | Nvidia          | GeForce RTX 4070       |   71.91$ |
| #683908 | Samsung         | Odyssey G7 27          |  407.29$ |
| #344840 | Razer           | DeathAdder V2          |  143.05$ |
| #386722 | Western Digital | WD Black SN850 1To     | 1862.27$ |
| #842536 | Asus            | ROG Strix G15          |  930.23$ |
| #082985 | Dell            | XPS 13                 | 2161.68$ |
| #304090 | Brother         | HL-L2350DW             |  806.14$ |
| #468344 | Western Digital | WD Black SN850 1To     | 1979.70$ |
| #822049 | Brother         | HL-L2350DW             |  432.13$ |
| #564293 | Samsung         | Odyssey G7 27          | 1963.23$ |
| #877050 | Kingston        | Fury Beast 16Go DDR5   |  247.47$ |
| #257912 | Lenovo          | ThinkPad X1 Carbon     | 1626.87$ |
| #293968 | Razer           | DeathAdder V2          | 1971.47$ |
| #442377 | Corsair         | K70 RGB Pro            | 2004.41$ |
| #398117 | Apple           | MacBook Air M2         |  980.25$ |
| #160152 | HP              | Pavilion 15            |  771.07$ |
| #873196 | Logitech        | MX Keys                | 1783.42$ |
| #761761 | Kingston        | Fury Beast 16Go DDR5   |  932.22$ |
| #705428 | HP              | Pavilion 15            | 1125.78$ |
| #258166 | Sony            | WH-1000XM5             |  942.52$ |
| #581505 | Nvidia          | GeForce RTX 4070       | 2293.94$ |
| #403791 | Apple           | MacBook Air M2         |  544.09$ |
| #188519 | Asus            | ROG Strix G15          |  635.14$ |
| #351253 | Nvidia          | GeForce RTX 4070       | 1614.14$ |
| #445388 | Nvidia          | GeForce RTX 4070       |  861.59$ |
| #961302 | Netgear         | Nighthawk AX12         | 1915.70$ |
| #120641 | Asus            | ROG Strix G15          | 1662.27$ |
| #556565 | Sony            | WH-1000XM5             |  389.38$ |
| #744593 | Kingston        | Fury Beast 16Go DDR5   | 1441.91$ |
| #024147 | Kingston        | Fury Beast 16Go DDR5   | 1184.73$ |
| #691443 | HP              | Pavilion 15            | 1742.22$ |
| #386075 | Acer            | Predator Helios 300    | 2342.83$ |
| #895171 | Acer            | Predator Helios 300    |  887.59$ |
| #453070 | Nvidia          | GeForce RTX 4070       | 1511.23$ |
| #561677 | Lenovo          | ThinkPad X1 Carbon     |  245.18$ |
| #107983 | Brother         | HL-L2350DW             |  420.16$ |
| #069953 | HP              | Pavilion 15            |  888.45$ |
| #278607 | Logitech        | MX Keys                | 1496.09$ |
| #910636 | Logitech        | MX Keys                |  530.84$ |
| #517729 | Acer            | Predator Helios 300    | 1973.64$ |
| #584780 | Apple           | MacBook Air M2         |  220.68$ |
| #612566 | Acer            | Predator Helios 300    | 1417.26$ |
| #352900 | Kingston        | Fury Beast 16Go DDR5   | 1925.60$ |
| #760213 | Netgear         | Nighthawk AX12         | 1691.39$ |
| #697716 | Sony            | WH-1000XM5             | 1541.38$ |
| #169231 | Kingston        | Fury Beast 16Go DDR5   | 2463.42$ |
| #900494 | Samsung         | Odyssey G7 27          | 2344.55$ |
| #479788 | Corsair         | K70 RGB Pro            | 2046.00$ |
| #722959 | Sony            | WH-1000XM5             |  503.13$ |
| #708585 | Brother         | HL-L2350DW             | 2035.69$ |
| #439291 | Acer            | Predator Helios 300    | 2311.19$ |
| #495139 | Apple           | MacBook Air M2         |  777.70$ |
| #441137 | Logitech        | MX Keys                | 1005.01$ |
| #329335 | Asus            | ROG Strix G15          | 2411.00$ |
| #379549 | Netgear         | Nighthawk AX12         | 2323.45$ |
| #614261 | Western Digital | WD Black SN850 1To     |  689.39$ |
| #961279 | Brother         | HL-L2350DW             | 1495.53$ |
| #344333 | Razer           | DeathAdder V2          |  277.64$ |
| #002758 | HP              | Pavilion 15            | 1257.35$ |
| #004364 | HP              | Pavilion 15            | 1163.36$ |
| #041011 | Lenovo          | ThinkPad X1 Carbon     |  209.73$ |
| #069039 | Razer           | DeathAdder V2          | 1279.98$ |
| #882560 | HP              | Pavilion 15            | 1977.80$ |
| #022934 | Kingston        | Fury Beast 16Go DDR5   | 1523.12$ |
| #529149 | Acer            | Predator Helios 300    | 1794.77$ |
| #040558 | Lenovo          | ThinkPad X1 Carbon     | 1873.59$ |
| #573802 | Logitech        | MX Keys                | 1487.54$ |
| #594527 | Sony            | WH-1000XM5             |   82.40$ |
| #575431 | Samsung         | Odyssey G7 27          | 2349.45$ |
| #764774 | Sony            | WH-1000XM5             | 1381.56$ |
| #101889 | Brother         | HL-L2350DW             | 1235.41$ |
| #408560 | HP              | Pavilion 15            | 2029.22$ |
| #362771 | Dell            | XPS 13                 |  999.57$ |
| #832582 | Razer           | DeathAdder V2          | 1480.43$ |
| #798808 | Logitech        | MX Keys                | 2129.26$ |
| #365528 | Lenovo          | ThinkPad X1 Carbon     | 1542.11$ |
| #192355 | Apple           | MacBook Air M2         | 1001.49$ |
| #292882 | Samsung         | Odyssey G7 27          |  933.18$ |
| #369074 | Apple           | MacBook Air M2         |  147.35$ |
| #825877 | Brother         | HL-L2350DW             |  259.90$ |
| #007626 | Corsair         | K70 RGB Pro            | 2125.09$ |
| #921405 | Apple           | MacBook Air M2         | 1141.77$ |
| #011764 | Logitech        | MX Keys                |  445.60$ |
| #554385 | Acer            | Predator Helios 300    |  670.64$ |
| #074708 | Lenovo          | ThinkPad X1 Carbon     | 1879.97$ |
| #793528 | Netgear         | Nighthawk AX12         |  187.63$ |
| #277014 | Acer            | Predator Helios 300    | 2053.73$ |
| #972606 | Razer           | DeathAdder V2          | 2461.97$ |
| #222262 | Razer           | DeathAdder V2          |  654.26$ |
| #424042 | Nvidia          | GeForce RTX 4070       |  164.13$ |
| #483759 | Razer           | DeathAdder V2          | 1149.13$ |
| #889102 | Dell            | XPS 13                 |  543.98$ |
| #360076 | Netgear         | Nighthawk AX12         |  418.57$ |
| #453582 | Dell            | XPS 13                 |  707.07$ |
| #807679 | Lenovo          | ThinkPad X1 Carbon     | 2444.62$ |
| #826455 | Acer            | Predator Helios 300    | 1579.29$ |
| #657794 | Sony            | WH-1000XM5             | 2091.54$ |
| #630509 | Kingston        | Fury Beast 16Go DDR5   |   97.72$ |
| #169320 | Nvidia          | GeForce RTX 4070       | 2022.25$ |
| #212144 | Samsung         | Odyssey G7 27          | 1445.80$ |
| #310847 | Dell            | XPS 13                 | 1593.09$ |
| #096781 | HP              | Pavilion 15            | 2279.58$ |
| #790323 | Samsung         | Odyssey G7 27          |  267.08$ |
| #767549 | HP              | Pavilion 15            |  717.32$ |
| #026387 | Lenovo          | ThinkPad X1 Carbon     | 1398.93$ |
| #855122 | Netgear         | Nighthawk AX12         | 1580.43$ |
| #487193 | Asus            | ROG Strix G15          | 1760.04$ |
| #015168 | Corsair         | K70 RGB Pro            | 2150.65$ |
| #974736 | Brother         | HL-L2350DW             | 1632.56$ |
| #539603 | Razer           | DeathAdder V2          |  268.28$ |
| #722668 | Razer           | DeathAdder V2          |  229.13$ |
| #000043 | Brother         | HL-L2350DW             |  415.13$ |
| #404486 | Asus            | ROG Strix G15          | 2201.36$ |
| #192395 | Logitech        | MX Keys                |  167.40$ |
| #180939 | Lenovo          | ThinkPad X1 Carbon     |  517.50$ |
| #987438 | Corsair         | K70 RGB Pro            |  524.65$ |
| #314282 | Netgear         | Nighthawk AX12         | 1347.31$ |
| #930006 | Dell            | XPS 13                 | 1853.22$ |
| #565601 | Sony            | WH-1000XM5             |  181.39$ |
| #827083 | Nvidia          | GeForce RTX 4070       | 1508.78$ |
| #683039 | Nvidia          | GeForce RTX 4070       |  234.94$ |
| #575620 | Apple           | MacBook Air M2         | 2169.41$ |
| #885664 | Sony            | WH-1000XM5             | 1044.18$ |
| #476948 | HP              | Pavilion 15            |  928.34$ |
| #029410 | Asus            | ROG Strix G15          | 1197.04$ |
| #387594 | Sony            | WH-1000XM5             |  712.84$ |
| #087312 | Netgear         | Nighthawk AX12         | 1502.92$ |
| #473567 | Samsung         | Odyssey G7 27          |  202.24$ |
| #878964 | Samsung         | Odyssey G7 27          |  461.33$ |
| #513064 | Netgear         | Nighthawk AX12         |  713.04$ |
| #487761 | Acer            | Predator Helios 300    |  370.06$ |
| #504362 | Samsung         | Odyssey G7 27          |  497.45$ |
| #772416 | Asus            | ROG Strix G15          | 1494.17$ |
| #714782 | Kingston        | Fury Beast 16Go DDR5   | 1954.94$ |
| #570024 | Lenovo          | ThinkPad X1 Carbon     | 1361.17$ |
| #763212 | Kingston        | Fury Beast 16Go DDR5   | 2344.66$ |
| #804508 | Western Digital | WD Black SN850 1To     |  135.77$ |
| #407040 | Netgear         | Nighthawk AX12         | 1106.70$ |
| #868436 | Kingston        | Fury Beast 16Go DDR5   | 2398.72$ |
| #094512 | Samsung         | Odyssey G7 27          |  134.09$ |
| #841693 | Acer            | Predator Helios 300    | 1146.18$ |
| #297743 | Samsung         | Odyssey G7 27          |  519.26$ |
| #880479 | Nvidia          | GeForce RTX 4070       |  989.29$ |
| #841644 | Kingston        | Fury Beast 16Go DDR5   |  104.56$ |
| #110017 | Acer            | Predator Helios 300    | 1647.63$ |
| #918811 | Acer            | Predator Helios 300    |  476.14$ |
| #494741 | Dell            | XPS 13                 | 1055.60$ |
| #053532 | Kingston        | Fury Beast 16Go DDR5   |  322.70$ |
| #381786 | Logitech        | MX Keys                |  546.33$ |
| #686235 | Lenovo          | ThinkPad X1 Carbon     | 1015.24$ |
| #239263 | Samsung         | Odyssey G7 27          | 1676.89$ |
| #411795 | Samsung         | Odyssey G7 27          | 1229.74$ |
| #768473 | Lenovo          | ThinkPad X1 Carbon     | 2489.58$ |
| #313822 | HP              | Pavilion 15            | 1366.85$ |
| #087263 | Apple           | MacBook Air M2         | 2289.50$ |
| #608455 | Razer           | DeathAdder V2          | 1452.36$ |
| #020527 | Logitech        | MX Keys                |  772.48$ |
| #488885 | Lenovo          | ThinkPad X1 Carbon     |  106.67$ |
| #960418 | Asus            | ROG Strix G15          | 1783.23$ |
| #231050 | Asus            | ROG Strix G15          |  969.03$ |
| #307398 | Nvidia          | GeForce RTX 4070       |  392.80$ |
| #583046 | Apple           | MacBook Air M2         | 1983.92$ |
| #342367 | Apple           | MacBook Air M2         | 1793.35$ |
| #627357 | Western Digital | WD Black SN850 1To     | 1502.39$ |
| #033500 | Brother         | HL-L2350DW             |  993.21$ |
| #075165 | HP              | Pavilion 15            | 1525.36$ |
| #597737 | Samsung         | Odyssey G7 27          |  880.19$ |
| #869006 | Dell            | XPS 13                 |  369.52$ |
| #213849 | Logitech        | MX Keys                |  406.18$ |
| #164366 | Asus            | ROG Strix G15          | 1054.29$ |
| #988812 | Western Digital | WD Black SN850 1To     | 1199.07$ |
| #005284 | Brother         | HL-L2350DW             | 1338.32$ |
| #958427 | Dell            | XPS 13                 | 1407.78$ |
| #313727 | Apple           | MacBook Air M2         |  921.46$ |
| #426820 | Sony            | WH-1000XM5             | 1409.41$ |
| #793149 | Brother         | HL-L2350DW             | 1042.83$ |
| #909287 | Netgear         | Nighthawk AX12         |  857.03$ |
| #610476 | Apple           | MacBook Air M2         | 2410.39$ |
| #151390 | Lenovo          | ThinkPad X1 Carbon     | 1431.71$ |
| #521143 | Dell            | XPS 13                 | 2217.97$ |
| #883835 | Kingston        | Fury Beast 16Go DDR5   |  446.66$ |
| #484998 | Kingston        | Fury Beast 16Go DDR5   | 1112.48$ |
| #023442 | Asus            | ROG Strix G15          |  411.92$ |
| #219915 | Western Digital | WD Black SN850 1To     | 1636.15$ |
| #002034 | Razer           | DeathAdder V2          |  580.29$ |
| #994884 | Lenovo          | ThinkPad X1 Carbon     | 2311.12$ |
| #241191 | Nvidia          | GeForce RTX 4070       | 2129.82$ |
| #109507 | Sony            | WH-1000XM5             | 1047.77$ |
| #342370 | Netgear         | Nighthawk AX12         |  217.77$ |
| #370199 | Corsair         | K70 RGB Pro            | 1460.68$ |
| #120192 | Corsair         | K70 RGB Pro            |  576.98$ |
| #905506 | Logitech        | MX Keys                | 1317.77$ |
| #221831 | Razer           | DeathAdder V2          |  846.61$ |
| #282459 | Apple           | MacBook Air M2         |  321.19$ |
| #442303 | Kingston        | Fury Beast 16Go DDR5   |  417.92$ |
| #835766 | Asus            | ROG Strix G15          | 1113.33$ |
| #100119 | Acer            | Predator Helios 300    |  696.38$ |
| #034719 | Lenovo          | ThinkPad X1 Carbon     | 2087.33$ |
| #419779 | Sony            | WH-1000XM5             |  781.25$ |
| #032803 | Acer            | Predator Helios 300    | 1699.82$ |
| #722776 | Apple           | MacBook Air M2         |  656.52$ |
| #572271 | Logitech        | MX Keys                | 1814.91$ |
| #296293 | Nvidia          | GeForce RTX 4070       |  163.47$ |
| #706729 | Apple           | MacBook Air M2         | 1204.87$ |
| #384393 | Western Digital | WD Black SN850 1To     | 1451.27$ |
| #118727 | Acer            | Predator Helios 300    |  951.54$ |
| #700206 | Samsung         | Odyssey G7 27          |  514.42$ |
| #376051 | Brother         | HL-L2350DW             | 1377.99$ |
| #873055 | Acer            | Predator Helios 300    |  187.04$ |
| #243211 | Apple           | MacBook Air M2         | 2466.97$ |
| #952626 | Sony            | WH-1000XM5             | 1569.61$ |
| #027606 | Lenovo          | ThinkPad X1 Carbon     | 1648.01$ |
| #730955 | Acer            | Predator Helios 300    |  390.61$ |
| #794215 | Nvidia          | GeForce RTX 4070       |  614.97$ |
| #611421 | Logitech        | MX Keys                | 2272.04$ |
| #701249 | Western Digital | WD Black SN850 1To     |  479.20$ |
| #046434 | Corsair         | K70 RGB Pro            | 1154.30$ |
| #907127 | Netgear         | Nighthawk AX12         | 2176.85$ |
| #575837 | Samsung         | Odyssey G7 27          |  130.23$ |
| #731364 | Apple           | MacBook Air M2         | 2203.20$ |
| #054631 | Dell            | XPS 13                 | 2464.31$ |
| #785871 | Razer           | DeathAdder V2          | 1387.79$ |
| #977703 | Logitech        | MX Keys                | 1087.68$ |
| #474455 | Brother         | HL-L2350DW             | 1878.96$ |
| #657937 | Samsung         | Odyssey G7 27          | 2355.25$ |
| #574659 | Brother         | HL-L2350DW             | 1358.13$ |
| #218981 | Logitech        | MX Keys                | 2330.80$ |
| #592798 | Corsair         | K70 RGB Pro            | 1412.75$ |
| #113285 | Sony            | WH-1000XM5             |  699.82$ |
| #769797 | Dell            | XPS 13                 | 2455.01$ |
| #618347 | Kingston        | Fury Beast 16Go DDR5   |  455.81$ |
| #970155 | Corsair         | K70 RGB Pro            | 1956.35$ |
| #639201 | Western Digital | WD Black SN850 1To     | 1698.18$ |
| #862424 | Brother         | HL-L2350DW             |  636.15$ |
| #297737 | Logitech        | MX Keys                | 1765.24$ |
| #067533 | Kingston        | Fury Beast 16Go DDR5   | 1064.69$ |
| #309472 | HP              | Pavilion 15            |   80.81$ |
| #455638 | Corsair         | K70 RGB Pro            | 1727.80$ |
| #753209 | Sony            | WH-1000XM5             |  445.32$ |
| #922588 | Kingston        | Fury Beast 16Go DDR5   | 2141.60$ |
| #266196 | HP              | Pavilion 15            | 1192.99$ |
| #687670 | Dell            | XPS 13                 | 2430.42$ |
| #178270 | HP              | Pavilion 15            | 1727.43$ |
| #572044 | Logitech        | MX Keys                |  799.74$ |
| #027076 | Asus            | ROG Strix G15          | 1344.91$ |
| #564526 | Acer            | Predator Helios 300    |  729.93$ |
| #994438 | Lenovo          | ThinkPad X1 Carbon     |  461.55$ |
| #990603 | Razer           | DeathAdder V2          |  224.89$ |
| #513262 | Nvidia          | GeForce RTX 4070       | 1602.69$ |
| #141354 | Kingston        | Fury Beast 16Go DDR5   | 1264.94$ |
| #193401 | Lenovo          | ThinkPad X1 Carbon     | 1148.00$ |
| #627511 | Asus            | ROG Strix G15          |  346.77$ |
| #780940 | Asus            | ROG Strix G15          |  456.82$ |
| #388699 | Sony            | WH-1000XM5             | 1918.99$ |
| #809273 | Brother         | HL-L2350DW             | 2229.56$ |
| #117043 | Razer           | DeathAdder V2          | 1830.47$ |
| #906486 | Dell            | XPS 13                 | 2139.33$ |
| #219109 | Lenovo          | ThinkPad X1 Carbon     |  332.89$ |
| #826067 | Apple           | MacBook Air M2         |  394.93$ |
| #933870 | Sony            | WH-1000XM5             | 1109.29$ |
| #002644 | Samsung         | Odyssey G7 27          |  818.98$ |
| #399267 | Brother         | HL-L2350DW             |  341.95$ |
| #810558 | HP              | Pavilion 15            | 2107.06$ |
| #953082 | Corsair         | K70 RGB Pro            | 1232.90$ |
| #038628 | Sony            | WH-1000XM5             | 2432.30$ |
| #206701 | Asus            | ROG Strix G15          | 2050.97$ |
| #444568 | Nvidia          | GeForce RTX 4070       | 2479.06$ |
| #157019 | Apple           | MacBook Air M2         | 2238.88$ |
| #453117 | HP              | Pavilion 15            | 1369.90$ |
| #540458 | Corsair         | K70 RGB Pro            |  539.81$ |
| #539880 | Dell            | XPS 13                 | 1114.83$ |
| #020808 | Dell            | XPS 13                 | 1209.14$ |
| #886616 | Nvidia          | GeForce RTX 4070       | 2386.87$ |
| #609670 | Netgear         | Nighthawk AX12         | 1670.79$ |
| #997112 | Corsair         | K70 RGB Pro            | 1580.82$ |
| #333389 | Nvidia          | GeForce RTX 4070       |  879.46$ |
| #561999 | Apple           | MacBook Air M2         | 1773.06$ |
| #077992 | Razer           | DeathAdder V2          | 1202.40$ |
| #588300 | Brother         | HL-L2350DW             |  702.45$ |
| #924693 | Corsair         | K70 RGB Pro            | 2421.99$ |
| #132045 | Nvidia          | GeForce RTX 4070       |   81.84$ |
| #647805 | HP              | Pavilion 15            | 2355.85$ |
| #486024 | Nvidia          | GeForce RTX 4070       |  565.86$ |
| #894835 | Samsung         | Odyssey G7 27          | 1707.22$ |
| #752704 | Western Digital | WD Black SN850 1To     | 1268.77$ |
| #316071 | Nvidia          | GeForce RTX 4070       |  683.22$ |
| #944131 | Acer            | Predator Helios 300    | 2348.52$ |
| #574227 | Western Digital | WD Black SN850 1To     | 2380.10$ |
| #752745 | Brother         | HL-L2350DW             |  212.45$ |
| #795088 | Apple           | MacBook Air M2         |  431.06$ |
| #232607 | Dell            | XPS 13                 |  469.66$ |
| #812086 | Lenovo          | ThinkPad X1 Carbon     |  623.23$ |
| #879356 | Western Digital | WD Black SN850 1To     | 2390.87$ |
| #059124 | Nvidia          | GeForce RTX 4070       | 1501.01$ |
| #794393 | Kingston        | Fury Beast 16Go DDR5   | 1933.18$ |
| #312686 | Corsair         | K70 RGB Pro            | 2021.06$ |
| #031618 | Nvidia          | GeForce RTX 4070       |  571.18$ |
| #502504 | Netgear         | Nighthawk AX12         |   94.63$ |
| #497431 | Logitech        | MX Keys                |  928.21$ |
| #594054 | Kingston        | Fury Beast 16Go DDR5   |  404.35$ |
| #605590 | Logitech        | MX Keys                |  728.60$ |
| #648563 | Netgear         | Nighthawk AX12         | 1674.92$ |
| #685019 | Sony            | WH-1000XM5             | 1074.00$ |
| #412107 | Razer           | DeathAdder V2          | 1489.23$ |
| #969614 | Apple           | MacBook Air M2         | 1541.18$ |
| #354224 | Apple           | MacBook Air M2         | 1971.26$ |
| #412141 | Sony            | WH-1000XM5             |  714.55$ |
| #565096 | Dell            | XPS 13                 |  411.98$ |
| #205855 | Razer           | DeathAdder V2          |  663.85$ |
| #044541 | Western Digital | WD Black SN850 1To     |  202.20$ |
| #096184 | Samsung         | Odyssey G7 27          |  148.67$ |
| #505202 | Kingston        | Fury Beast 16Go DDR5   | 2048.08$ |
| #129513 | Apple           | MacBook Air M2         | 1143.61$ |
| #317783 | Samsung         | Odyssey G7 27          | 1910.10$ |
| #191144 | Nvidia          | GeForce RTX 4070       | 1542.50$ |
| #012893 | HP              | Pavilion 15            |  404.07$ |
| #373315 | Acer            | Predator Helios 300    | 1797.07$ |
| #827627 | Corsair         | K70 RGB Pro            |  873.13$ |
| #199605 | Netgear         | Nighthawk AX12         | 1896.81$ |
| #754139 | Samsung         | Odyssey G7 27          | 1323.75$ |
| #169689 | Logitech        | MX Keys                |  446.68$ |
| #783595 | Logitech        | MX Keys                | 2285.96$ |
| #806580 | Western Digital | WD Black SN850 1To     |  676.21$ |
| #538255 | Dell            | XPS 13                 |  677.74$ |
| #924086 | Asus            | ROG Strix G15          | 1264.46$ |
| #809453 | Kingston        | Fury Beast 16Go DDR5   | 2196.03$ |
| #635575 | Lenovo          | ThinkPad X1 Carbon     |  255.71$ |
| #608880 | Lenovo          | ThinkPad X1 Carbon     | 2441.05$ |
| #210046 | Kingston        | Fury Beast 16Go DDR5   | 1836.88$ |
| #443371 | Dell            | XPS 13                 |  969.72$ |
| #258462 | Asus            | ROG Strix G15          |  876.24$ |
| #795822 | Logitech        | MX Keys                | 1673.72$ |
| #966123 | Apple           | MacBook Air M2         | 2199.64$ |
| #480752 | Apple           | MacBook Air M2         | 1323.91$ |
| #655747 | Corsair         | K70 RGB Pro            |  957.76$ |
| #878151 | Samsung         | Odyssey G7 27          | 2163.59$ |
| #506486 | Brother         | HL-L2350DW             | 1691.87$ |
| #326800 | Kingston        | Fury Beast 16Go DDR5   |  372.96$ |
| #358605 | Lenovo          | ThinkPad X1 Carbon     |   65.88$ |
| #781804 | Lenovo          | ThinkPad X1 Carbon     | 1115.41$ |
| #488395 | Apple           | MacBook Air M2         | 1968.00$ |
| #813929 | Razer           | DeathAdder V2          | 2168.25$ |
| #472647 | Sony            | WH-1000XM5             | 1187.32$ |
| #153748 | Corsair         | K70 RGB Pro            | 1415.46$ |
| #995091 | HP              | Pavilion 15            | 2265.99$ |
| #050441 | Lenovo          | ThinkPad X1 Carbon     | 2277.50$ |
| #695788 | Western Digital | WD Black SN850 1To     | 1470.50$ |
| #440460 | Razer           | DeathAdder V2          | 1696.92$ |
| #983925 | Netgear         | Nighthawk AX12         |  432.27$ |
| #583261 | Nvidia          | GeForce RTX 4070       | 1465.70$ |
| #160965 | Asus            | ROG Strix G15          | 1016.04$ |
| #176081 | Sony            | WH-1000XM5             |  781.83$ |
| #741971 | Dell            | XPS 13                 | 1271.40$ |
| #332286 | Razer           | DeathAdder V2          | 1899.19$ |
| #807743 | Brother         | HL-L2350DW             |  500.83$ |
| #505387 | Logitech        | MX Keys                | 2407.73$ |
| #459346 | Apple           | MacBook Air M2         | 1633.34$ |
| #574454 | Brother         | HL-L2350DW             |  623.84$ |
| #956573 | Kingston        | Fury Beast 16Go DDR5   | 2058.16$ |
| #808745 | HP              | Pavilion 15            | 1312.69$ |
| #169675 | Razer           | DeathAdder V2          |  959.48$ |
| #815673 | Razer           | DeathAdder V2          | 1383.32$ |
| #280739 | Netgear         | Nighthawk AX12         |  431.75$ |
| #584525 | Western Digital | WD Black SN850 1To     | 1672.11$ |
| #018326 | Nvidia          | GeForce RTX 4070       |  552.37$ |
| #557555 | Samsung         | Odyssey G7 27          |  291.20$ |
| #005766 | Nvidia          | GeForce RTX 4070       | 1937.02$ |
| #900400 | Kingston        | Fury Beast 16Go DDR5   | 1119.28$ |
| #817300 | Sony            | WH-1000XM5             | 2432.45$ |
| #891914 | Acer            | Predator Helios 300    | 1469.66$ |
| #593904 | Asus            | ROG Strix G15          |  366.03$ |
| #311660 | HP              | Pavilion 15            |  308.71$ |
| #666902 | Netgear         | Nighthawk AX12         | 1364.92$ |
| #846184 | Western Digital | WD Black SN850 1To     |  193.47$ |
| #504614 | Corsair         | K70 RGB Pro            | 1594.23$ |
| #838638 | Brother         | HL-L2350DW             | 1582.30$ |
| #499286 | Sony            | WH-1000XM5             |  779.63$ |
| #434330 | Dell            | XPS 13                 |   50.99$ |
| #686229 | Acer            | Predator Helios 300    |  169.80$ |
| #764694 | Nvidia          | GeForce RTX 4070       | 1206.47$ |
| #985914 | HP              | Pavilion 15            |  923.33$ |
| #814342 | Nvidia          | GeForce RTX 4070       | 2156.04$ |
| #336635 | Western Digital | WD Black SN850 1To     | 1799.36$ |
| #890121 | Netgear         | Nighthawk AX12         | 1455.68$ |
| #301846 | Acer            | Predator Helios 300    | 1015.69$ |
| #120034 | Logitech        | MX Keys                |   91.66$ |
| #288368 | Samsung         | Odyssey G7 27          | 2274.34$ |
| #264896 | Razer           | DeathAdder V2          | 1939.03$ |
| #378939 | Razer           | DeathAdder V2          | 2206.72$ |
| #779299 | Apple           | MacBook Air M2         | 1417.05$ |
| #279136 | Apple           | MacBook Air M2         | 1382.20$ |
| #400363 | Lenovo          | ThinkPad X1 Carbon     | 1264.29$ |
| #787670 | HP              | Pavilion 15            | 1945.19$ |
| #937342 | Nvidia          | GeForce RTX 4070       | 1024.68$ |
| #922391 | Razer           | DeathAdder V2          |  761.37$ |
| #094426 | Kingston        | Fury Beast 16Go DDR5   |  143.72$ |
| #920676 | Corsair         | K70 RGB Pro            | 1810.18$ |
| #789871 | Dell            | XPS 13                 | 1472.96$ |
| #225315 | Apple           | MacBook Air M2         | 2270.39$ |
| #208827 | Western Digital | WD Black SN850 1To     |  333.36$ |
| #614706 | Dell            | XPS 13                 | 1142.03$ |
| #298086 | Western Digital | WD Black SN850 1To     | 2233.76$ |
| #479511 | Corsair         | K70 RGB Pro            | 1433.65$ |
| #240832 | Logitech        | MX Keys                | 1884.35$ |
| #058001 | Logitech        | MX Keys                |  847.76$ |
| #649035 | Sony            | WH-1000XM5             | 1404.58$ |
| #954636 | Sony            | WH-1000XM5             | 1285.38$ |
| #741699 | Western Digital | WD Black SN850 1To     | 1665.72$ |
| #196891 | HP              | Pavilion 15            | 1622.83$ |
| #689311 | Sony            | WH-1000XM5             |  711.95$ |
| #594078 | Apple           | MacBook Air M2         | 2021.98$ |
| #590502 | Brother         | HL-L2350DW             | 1013.19$ |
| #130592 | Samsung         | Odyssey G7 27          | 1951.27$ |
| #664141 | Kingston        | Fury Beast 16Go DDR5   | 2420.77$ |
| #529947 | Nvidia          | GeForce RTX 4070       |  848.43$ |
| #126073 | Brother         | HL-L2350DW             | 2278.35$ |
| #857298 | Asus            | ROG Strix G15          |  231.34$ |
| #601321 | Corsair         | K70 RGB Pro            |  158.33$ |
| #582701 | Dell            | XPS 13                 |  115.30$ |
| #344140 | Acer            | Predator Helios 300    |  885.01$ |
| #001158 | Kingston        | Fury Beast 16Go DDR5   | 1575.74$ |
| #401577 | Apple           | MacBook Air M2         | 1928.21$ |
| #298914 | Logitech        | MX Keys                |  880.67$ |
| #711791 | Lenovo          | ThinkPad X1 Carbon     |  963.50$ |
| #062307 | Asus            | ROG Strix G15          | 1548.66$ |
| #899293 | Dell            | XPS 13                 |  251.04$ |
| #081279 | Western Digital | WD Black SN850 1To     | 2287.27$ |
| #273106 | Dell            | XPS 13                 |  949.32$ |
| #315352 | Nvidia          | GeForce RTX 4070       | 1881.46$ |
| #401705 | Logitech        | MX Keys                | 2436.62$ |
| #039601 | Netgear         | Nighthawk AX12         |  418.67$ |
| #267444 | Brother         | HL-L2350DW             |  245.18$ |
| #392085 | Razer           | DeathAdder V2          | 1606.88$ |
-----------------------------------------------------------------
```

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
