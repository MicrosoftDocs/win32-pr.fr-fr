---
title: Unions RPC
description: Les unions encapsulées et sans encapsulées, ainsi que leur format avec appel de procédure distante (RPC).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011388"
---
# <a name="rpc-unions"></a>Unions RPC

Les unions encapsulées et non encapsulées partagent un sélecteur de bras d’Union commun \_ \_<> format :

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

Le \_ champ des bras d’union<2> se compose de deux parties. Si l’Union est une Union de style MIDL 1,0, les 4 bits de poids fort contiennent l’alignement du bras d’Union (alignement du bras le plus aligné). Sinon, les 4 bits supérieurs sont nuls. Les 12 bits inférieurs contiennent le nombre de branches dans l’Union. En d’autres termes :

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

La \_ Description de décalage à \_ ARM \_<2> champs contiennent un offset signé relatif à la description de type du ARM. Toutefois, le champ est surchargé avec l’optimisation pour les types simples. Pour ceux-ci, l’octet supérieur de ce champ de décalage est l’octet de l' \_ Union magique FC \_ \_ (0x80) et l’octet de poids faible est le type de caractère de format réel du bras. Par conséquent, il existe deux plages pour les valeurs de décalage : « 80 *XX*» signifie que *XX* est une chaîne de format de type ; et tout le reste dans la plage (80 FF.. 7F FF) signifie un décalage réel. Cela fait des décalages de la plage <80 00. 80 FF > non disponible comme décalages. Le compilateur vérifie que la version de MIDL 5.1.164.

Le \_ \_ champ de description ARM<2> par défaut indique le type de bras d’Union pour le bras par défaut, le cas échéant. Si aucun ARM par défaut n’est spécifié pour l’Union, la \_ Description du ARM par défaut \_<2> champ est 0xFFFF et une exception est levée si le commutateur \_ est une valeur ne correspond à aucune des valeurs de cas ARM. Si le ARM par défaut est spécifié mais vide, la description du ARM par défaut \_ \_<2> champ est égal à zéro. Dans le cas contraire, la description du ARM par défaut \_ \_<2> champ a la même sémantique que la description du décalage \_ vers \_ ARM \_<2> champs.

Voici un résumé :

-   0-valeur par défaut vide
-   FFFF-pas de valeur par défaut
-   80xx-type simple
-   autre décalage relatif

## <a name="encapsulated-unions"></a>Unions encapsulées

Une Union encapsulée provient d’une syntaxe d’Union spéciale dans IDL. En effet, une Union encapsulée est une structure de regroupement avec un champ discriminante au début de la structure et l’Union comme seul autre membre.

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

Le type de commutateur d’une Union encapsulée \_<1> champ a deux parties. Le Quartet inférieur fournit le type de commutateur réel, et le Quartet supérieur fournit l’incrément de mémoire pour effectuer un pas à pas principal, ce qui indique que le pointeur de la mémoire doit être incrémenté afin de ne pas dépasser le champ du commutateur \_ , ce qui inclut le remplissage entre le champ Switch \_ is () de la structure construite par stub et le champ Union réel.

La \_ taille de la mémoire<2> champ est la taille de l’Union uniquement et est identique aux unions non encapsulées. Pour obtenir la taille totale de la structure qui contient l’Union, ajoutez la taille de la mémoire \_<2> à l’incrément de mémoire pour effectuer un pas à pas principal, c’est-à-dire au Quartet supérieur du type de commutateur \_<1> champ, puis alignez par l’alignement correspondant à l’incrément.

## <a name="nonencapsulated-unions"></a>Unions qui ne sont pas encapsulées

Une Union non encapsulée est une situation classique dans laquelle une Union est un argument ou un champ et le commutateur est un autre argument ou champ, respectivement.

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

Où :

Le \_ type de commutateur<1> champ est un caractère de format pour le discriminante.

Le commutateur \_ est un descripteur \_<> champ est un descripteur de corrélation et a 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non. Toutefois, pour le commutateur \_ est la \_ Description<>, si l’Union est incorporée dans une structure, le champ de décalage du commutateur \_ est la \_ Description<> le décalage par \_ rapport au commutateur est le champ de la position de l’Union dans la structure (pas à partir du début de la structure).

La \_ Description offset to \_ size \_ and \_ ARM \_<2> champ donne le décalage à la description de la taille et du ARM de l’Union, ce qui est identique à celui des unions encapsulées et est partagé par toutes les unions non encapsulées du même type :

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 