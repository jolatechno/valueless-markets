# Marchés sans valeurs - _méthodes pour le prix libre_

## _Valueless markets - methods for setting free prices_

[![fr](https://img.shields.io/badge/lang-fr-red.svg)](./Readme.avec-math.md)
[![en](https://img.shields.io/badge/lang-en-green.svg)](./Readme.with-math.en.md)

Cette page est la version avec les détails mathématiques, vous pouvez aussi lire [la version _sans_ math](Readme.md).

À terme des examples (sans doute sous le format de tableurs) et/ou des outils d'implémentation des méthodes proposées ici (tableurs, peut-être programes python simple et/ou autre outil de comptabilité adapté) seront ajoutés à ce dépot.

## 1 - Introduction

**Motivation :** _À écrire_

**Pourquoi ce nom :** _À écrire_

**À quoi ca ne répond pas :** _À écrire_

**Mise en place :** _À écrire (information partielle)_

## 2 - Méthodes

### 2.1 - Achat à prix libre, vente à prix fixe

_À écrire_

Chaque acheteur·ice donne un prix désiré (ou prix idéal) et un prix maximum qu'iel est prêt·e à payer pour sa commande. Le but est de trouvé quel ratio $\alpha$ entre le prix désiré et le prix maximum de tout les acheteur·ice permetra de finaliser la commande.

| **_Situation_** | La somme des prix maximum est inferieur au coût d'achat. | La somme des prix maximum est égale au coût d'achat. | Le coût d'achat est entre (la moyenne de) la somme des prix maximum et prix désirés. | La somme des prix désirés est égale au coût d'achat. | La somme des prix désirés est deux fois plus haute que le coût d'achat. |
|  :----------------  | :------: | :------:  |  :------:  | :------: | :------: |
| $\alpha$ | _blocage_ | 0 | 0.5 | 1 | 2 |
| **_Coûts pour les acheteur·ices_** | _L'achat n'est pas possible._ | Les acheteur·ices payent leur prix maximum d'achat. | Les acheteur·ices payent entre (la moyenne de) leur prix maximum et désiré. | Les acheteur·ices payent leur prix désiré. | Les acheteur·ices payent la moitié de leur prix désiré. |

**Condition de blocage :** Un blocage peut aparaitre si la somme des prix maximum des acheteur·ices est inferieur au cout d'achat. Dans ce cas il ne sera pas possible de finaliser l'achat en répsectant les régles simple proposées au dessus.

#### 2.1.a - Résolution des blocage

**Prunage/supression des achats problèmatique (_pas necessairement désirable !_) :** _À écrire_

**Utilisation d'une caisse de trésorerie :**  _À écrire_

### 2.2 - Achat et vente à prix libre

_À écrire_

Chaque acheteur·ice donne un prix désiré (ou prix idéal) et un prix maximum qu'iel est prêt·e à payer pour sa commande, et chaque vendeur·euse donne un prix désiré (ou idéal) et un prix minimum qu'iel peut se permettre de resevoir en échange de sa production. Le but est de trouvé quel ratio $\alpha$ entre le prix désiré et le prix maximum/minimum de tout les acheteur·ice et vendeur·euse permetra de finaliser la commande.


| **_Situation_** | La somme des prix maximum des acheteur·ices est inferieur à la somme des prix minimum des vendeur·euses. | La somme des prix maximum est égale à la somme des prix minimum des vendeur·euses. | La moyenne entre la somme des prix maximum et prix désirés des acheteur·ices est églae à la moyenne entre la somme des prix minimum et prix désirés des vendeur·euses. | La somme des prix désirés des acheteur·ices est égale à la somme des prix désirés des vendeur·euses. | La somme des prix désirés des acheteur·ices est deux fois plus haute que la somme des prix désirés des vendeur·euses. |
|  :----------------  | :------: | :------:  |  :------:  | :------: | :------: |
| $\alpha$ | _blocage_ | 0 | 0.5 | 1 | 2 |
| **_Coûts pour les acheteur·ices_** | _L'achat n'est pas possible._ | Les acheteur·ices payent leur prix maximum d'achat. | Les acheteur·ices payent entre (la moyenne de) leur prix maximum et désiré. | Les acheteur·ices payent leur prix désiré. | Les acheteur·ices payent 70% ($\frac{1}{\sqrt{2}}$) de leur prix désiré. |
| **_Gains pour les vendeur·euses_** | _L'achat n'est pas possible._ | Les vendeur·euses sont payé·es leur prix minimum de vente. | Les vendeur·euses sont payé·es entre (la moyenne de) leur prix minimum et désiré. | Les payé·es sont payé·es leur prix désiré. | Les vendeur·euses sont payé·es 40% de plus ($\frac{1}{\sqrt{2}}$) que leur prix désiré. |


**Condition de blocage :** Un blocage peut aparaitre si la somme des prix maximum des acheteur·ices est inferieur à la somme des revenus minimum des vendeur·euses. Dans ce cas il ne sera pas possible de finaliser l'achat en répsectant les régles simple proposées au dessus.

**Quelques cas particuliers :** _À écrire_

#### 2.2.a - Résolution des blocage

**Prunage/supression des achats problèmatique (_pas necessairement désirable !_) :** _À écrire_

**Prunage/supression des ventes problèmatique (_pas necessairement désirable !_) :** _À écrire_

**Utilisation d'une caisse de trésorerie :**  _À écrire_

### 2.3 - Achat et vente à prix libre, stock imparfait

_À écrire_