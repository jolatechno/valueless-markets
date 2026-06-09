# Marchés sans valeurs - _méthodes pour le prix libre_

## _Valueless markets - methods for setting free prices_

[![fr](https://img.shields.io/badge/lang-fr-red.svg)](./Readme.avec-math.md)
[![en](https://img.shields.io/badge/lang-en-green.svg)](./Readme.with-math.en.md)

Cette page est la version avec les détails mathématiques, vous pouvez aussi lire [la version _sans_ math](Readme.md).

À terme des examples (sans doute sous le format de tableurs) et/ou des outils d'implémentation des méthodes proposées ici (tableurs, peut-être programes python simple et/ou autre outil de comptabilité adapté) seront ajoutés à ce dépot.

## 1 - Introduction

**Motivation :** Le prix libre (_fait que chaque personne puisse payer ce qu'iel veut_) marche bien dans pas mal de situation et permet aux acheteur·ices d'adapter le prix en fonction de leur besoin et de leurs capacités, mais quand le revenu de certaine personne dépend de la vente la peur de ne pas pouvoir se payer à tendance à ramener vers un prix fixe. L'idée des méthode proposées ici est de facilier une forme de prix libre tout en garantissant que les cout soient récuperer.

**Pourquoi ce nom :** Le nom de "marchés sans valeurs" vient de l'idée que ces méthodes servent à faire des marchés (dans le sens de lieu/outil de vente) mais où les prix ne sont pas relié à la valeur marchande des produit vendu mais plutot aux besoins et capacités des acheteur·ices et des vendeur·euses.

**À quoi ca ne répond pas :** Aucune méthode ne peut regler tout les problème, le but n'est pas de remplacer l'organsiation et la discussion par un outil mathématique. Dans certaines situation negocier, s'organiser et fonctionner sans echange d'argent peut être préférable. Mais dans le cadre de groupe d'achat, d'AMAP, etc... avoir un outil sur lequel reposer peut simplifier grandement le fonctionnement et réduire la barrière d'entrée (tout le monde ne veut pas 4h d'AG et de négociation avant de faire une commande dans un groupe d'achat).

**Mise en place :** En pratique la majorité de ces méthode repose sur le fait de se faire passer un tableur colaboratif, et que chaque acheteur·ice (et parfois vendeur·euse) remplisse ce qu'iel souhaite acheter et donne leur prix désiré et leur prix maximum. Pour éviter que des personnes cherchent à savoir si ce qu'iel payent est "dans la moyenne" alors que le but est que chacun se demande ce qu'iel peut payer independement de la valeur des biens, ca peut être préférable de mettre en place un system pour que personnes ne voit les commandes et prix donnés par les autres.

## 2 - Méthodes

### 2.1 - Achat à prix libre, vente à prix fixe

La première méthode proposée est la plus simple, et s'applique aux situation où les vendeur·euses ne vendent pas à prix libre (donc typiquement dans le cadre d'un groupe d'achat où on fait une commande groupée à un commercant classique).

Chaque acheteur·ice donne un prix désiré (ou prix idéal) et un prix maximum qu'iel est prêt·e à payer pour sa commande. Le but est de trouvé quel ratio $\alpha$ entre le prix désiré et le prix maximum de tout les acheteur·ice permetra de finaliser la commande. À noter que si les acheteur·ices sur-estime les coût iels payeront moins que leur prix désiré.

| **_Situation_** | La somme des prix maximum est inferieur au coût d'achat. | La somme des prix maximum est égale au coût d'achat. | Le coût d'achat est entre (la moyenne de) la somme des prix maximum et prix désirés. | La somme des prix désirés est égale au coût d'achat. | La somme des prix désirés est deux fois plus haute que le coût d'achat. |
|  :----------------  | :------: | :------:  |  :------:  | :------: | :------: |
| $\alpha$ | _blocage_ | 0 | 0.5 | 1 | 2 |
| **_Coûts pour les acheteur·ices_** | _L'achat n'est pas possible._ | Les acheteur·ices payent leur prix maximum d'achat. | Les acheteur·ices payent entre (la moyenne de) leur prix maximum et désiré. | Les acheteur·ices payent leur prix désiré. | Les acheteur·ices payent la moitié de leur prix désiré. |

**Condition de blocage :** Un blocage peut aparaitre si la somme des prix maximum des acheteur·ices est inferieur au cout d'achat. Dans ce cas il ne sera pas possible de finaliser l'achat en répsectant les régles simple proposées au dessus.

#### 2.1.a - Résolution des blocage

Si un blocage apparait (ce qui idéalement n'arrive pas), l'idéal est d'en parler, pour voir si la commande doit être annulé, ou si des personnes peuvent se permettre d'augmenter leur prix maximum. Il peut aussi y avoir d'autre strategies pour résoudre "automatiquement" ces blocages.

**Prunage/supression des achats problèmatique (_pas necessairement désirable !_) :** Une solution peut être de supprimer les commandes qui participent le plus au blocage (donc les commandes dont le prix maximum est le plus faible par rapport au prix de vente des produit). Mais c'est quasiment jamais désirable car ca veut dire interdire la commande aux gens qui sont sans doute les plus précaire.

**Utilisation d'une caisse de trésorerie :**  Une autre solution peut être de combler le manque entre la somme des prix maximum des acheteur·ices et le coût d'achat par de l'argent qui sort d'une caisse de trésorerie. Cette caisse peut être rempli par une cotisation, ou peut se reremplir pendant les autres commandes en la rajoutant une cotisation aux coût d'achat de la prochaine commande (l'avantage étant que la part de la cotisation de chacun dépend alors des prix désiré et maximum des acheteur·ices). À noter que dans la prochaine méthode la gestion de cette caisse est plus évidente.

### 2.2 - Achat et vente à prix libre

La seconde méthode proposée s'applique aux situation où les vendeur·euses vendent aussi à prix libre. Le plus simple pour cette méthode est de d'abord recenser ce que les acheteur·ices veulent acheter, puis demander aux vendeur·euses de completer le prix auquel iels peuvent vendre ces quantités totales. La méthode 2.3 proposera une solution pour que les deux se fasse en simultané.

Chaque acheteur·ice donne un prix désiré (ou prix idéal) et un prix maximum qu'iel est prêt·e à payer pour sa commande, et chaque vendeur·euse donne un prix désiré (ou idéal) et un prix minimum qu'iel peut se permettre de resevoir en échange de sa production. Le but est de trouvé quel ratio $\alpha$ entre le prix désiré et le prix maximum/minimum de tout les acheteur·ice et vendeur·euse permetra de finaliser la commande. À noter que si les acheteur·ices sur-estime les coût et/ou que les vendeur·euses sous-estime les prix, les acheteur·ices payeront moins que leur prix désiré, et les vendeur·euses seront mieux payé que leur prix désiré.

| **_Situation_** | La somme des prix maximum des acheteur·ices est inferieur à la somme des prix minimum des vendeur·euses. | La somme des prix maximum est égale à la somme des prix minimum des vendeur·euses. | La moyenne entre la somme des prix maximum et prix désirés des acheteur·ices est églae à la moyenne entre la somme des prix minimum et prix désirés des vendeur·euses. | La somme des prix désirés des acheteur·ices est égale à la somme des prix désirés des vendeur·euses. | La somme des prix désirés des acheteur·ices est deux fois plus haute que la somme des prix désirés des vendeur·euses. |
|  :----------------  | :------: | :------:  |  :------:  | :------: | :------: |
| $\alpha$ | _blocage_ | 0 | 0.5 | 1 | 2 |
| **_Coûts pour les acheteur·ices_** | _L'achat n'est pas possible._ | Les acheteur·ices payent leur prix maximum d'achat. | Les acheteur·ices payent entre (la moyenne de) leur prix maximum et désiré. | Les acheteur·ices payent leur prix désiré. | Les acheteur·ices payent 70% ($\frac{1}{\sqrt{2}}$) de leur prix désiré. |
| **_Gains pour les vendeur·euses_** | _L'achat n'est pas possible._ | Les vendeur·euses sont payé·es leur prix minimum de vente. | Les vendeur·euses sont payé·es entre (la moyenne de) leur prix minimum et désiré. | Les vendeur·euses sont payé·es leur prix désiré. | Les vendeur·euses sont payé·es 40% de plus ($\frac{1}{\sqrt{2}}$) que leur prix désiré. |

**Condition de blocage :** Un blocage peut aparaitre si la somme des prix maximum des acheteur·ices est inferieur à la somme des revenus minimum des vendeur·euses. Dans ce cas il ne sera pas possible de finaliser l'achat en répsectant les régles simple proposées au dessus.

#### 2.2.a - Cas particuliers

Cette méthode étant plus fléxible, on peut proposer quelques cas d'usage particulier.

**Cout de fonctionnement :** Un coût de fonctionnement peut être ajouter aux vendeur·euses. Par exemple si le collectif qui utilise cette méthode est hebergé dans un lieu qui lui coûte 100 euros par mois, et qu'idéalement il faudrait acheter des outils pour l'entretient à 200 euros, alors le collectif peut ajouter un vendeur avec un prix de vente minimum à 100 euros pour garentir que le loyer sera payer, et un prix idéal à 300 euro pour que si il y a de l'excedant les outils puissent être acheté. Ce qui sera récupérer dépend alors d'à quel point les prix des acheteur·ices sont haut par rapport aux prix des vendeur·euses, et la part de cotisation au lieu de chaque acheteur·ice dépend alors de son prix idéal et maximum d'achat.

**Remplissage d'une caisse de trésorerie :** Une caisse pour amortir les blocage peut être remplie par une cotisation comme décrit dans le paragraph précedent. C'est aussi possible que dans le cas d'une vente où la somme des prix idéal des acheteur·ices est supérieur à la somme des prix idéal des vendeur·euses (donc $\alpha > 1$) le surplus soit capté dans la caisse plutôt que redistribué comme la méthode le prévoit.

#### 2.2.b - Résolution des blocage

Pour résoudre les blocages pour cette méthode les solution "automatiques" sont :

**Prunage/supression des achats problèmatique (_pas necessairement désirable !_) :** Une solution peut être de supprimer les commandes des acheteur·ices qui participent le plus au blocage comme décrit plus haut. Mais c'est quasiment jamais désirable car ca veut dire interdire la commande aux gens qui sont sans doute les plus précaire.

**Prunage/supression des ventes problèmatique (_pas necessairement désirable !_) :** Il est aussi possible de supprimer les produit acheter aux vendeur·euses qui participent le plus au blocages (donc dont les produit ont le plus haut prix demandé par rapport aux autres), mais tout comme pour les acheteur·ices ca pose problème car les vendeur·euses qui demandent les plus haut prix sont sans doute ceux qui sont le plus en difficulté et dont on ne veut donc pas interdir à participer à la vente.

**Utilisation d'une caisse de trésorerie :**  Comme decrit plus haut le déficit peut être combler par une caisse, qui peut être rempli de plusieurs manière.

### 2.3 - Achat et vente à prix libre, stock imparfait

Pour simplifier la coordination des acheteur·ices et des vendeur·euses, il est possible que chaque acheteur·ices note quel quantité d'un produit iel veut, et que chaque vendeur·euses note quelle quantité iel peut vendre. Ensuite la quantité vendu d'un produit est le minimum entre la somme des stock vendu et des stock demandé à l'achat.

Il y aura alors soit une proportion $1-\beta$ des demande des acheteur·ices qui ne sera pas rempli, ou des stock des vendeur·euses qui ne sera pas vendu. Si les objet vendu ne sont vendable qu'à l'unité pour réajuster par exemple 50 produit demandé mais seulement 30 vendu on peut utiliser la _methode proportionnelle avec plus fort reste_ (méthode utilisée dans les éléctions municipale francaise) pour assigner les 30 produit aux acheteur·ices en approchant le plus possible 3/5 de leur commande.

| **_Situation_** | Les acheteur·ices commande deux fois plus d'un produit que les vendeur·euses en vende. | Les acheteur·ices commande autant d'un produit que les vendeur·euses en vende. | Les acheteur·ices commande deux fois moins d'un produit que les vendeur·euses en vende. |
|  :----------------  | :------: | :------:  |  :------:  |
| $\beta$ | 0.5 | 1 | 0.5 |
| **_Quantité pour les acheteur·ices_** |  Les acheteur·ices recoivent seulement la moitié de leurs commandes. | Les acheteur·ices recoivent leur commande en entier. | Les acheteur·ices recoivent leur commande en entier.  |
| **_Quantité pour les vendeur·euses_** | Les vendeur·euses vendent l'entièreté de leur stock. | Les vendeur·euses vendent l'entièreté de leur stock. | Les vendeur·euses vendent la moitié de leur stock. |

Sachant que les stock vendu et acheté ne le sont pas entierement, il est possible de réajuster les prix de vente/achat selont plusieur strategies :
 - Si on sépare par produit les prix idéal, maximum et minimum, multiplier chaque prix par la proportion $\beta$ de la commande/vente qui sera obtenue/vendue.
 - Si il y a un surplus de stock à vendre et que la commande peut se faire sans blocage, faire la commande en achetant l'entièreté du stock, et soit redistribuer le surplus de stock proportionnelement aux acheteur·ices, soit le donner à des association ou autre. Ca permet de garentir aux vendeur·euses la vente de leur stock.
 - Accepter que au même prix on risque de ne recevoir qu'une partie de sa commande, il serait possible d'indiquer une limite, ou de demander la confirmation avant de confirmer la commande.