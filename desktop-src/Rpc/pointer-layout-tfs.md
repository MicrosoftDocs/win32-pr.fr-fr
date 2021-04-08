---
title: Disposition du pointeur
description: La disposition du pointeur décrit les pointeurs d’une structure ou d’un tableau.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840522"
---
# <a name="pointer-layout"></a>Disposition du pointeur

La disposition du pointeur décrit les pointeurs d’une structure ou d’un tableau.

## <a name="pointer_layout"></a>disposition du pointeur \_<>

Une disposition de pointeur \_<> champ se compose du bloc de format caractères FC \_ pp FC \_ suivi d’une ou de plusieurs descriptions de pointeur, comme décrit ultérieurement, et se terminant par un \_ caractère de format de fin FC :

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

Une \_ \_ disposition d’instance de pointeur<> champ est une chaîne de format décrivant une ou plusieurs instances de pointeurs. Les champs suivants sont utilisés dans ces descripteurs :

-   décalage \_ en \_ mémoire

    Décalage signé à l’emplacement du pointeur en mémoire. Pour un pointeur résidant dans une structure, cet offset est un décalage négatif par rapport à la fin de la structure (la fin de la partie non conforme des structures conformes); pour les tableaux, l’offset est à partir du début du tableau.

-   décalage \_ dans la \_ mémoire tampon

    Offset signé à l’emplacement du pointeur dans la mémoire tampon. Pour un pointeur résidant dans une structure, cet offset est un décalage négatif à partir de la fin de la structure (la fin de la partie non conforme des structures conformes) : pour les tableaux, l’offset est à partir du début du tableau.

-   décalage \_ vers le \_ tableau

    Offset d’une structure englobante vers le tableau incorporé dont les pointeurs sont gérés. Pour les tableaux de niveau supérieur, ce champ sera toujours égal à zéro.

-   itérations

    Nombre total de pointeurs ayant la même disposition<> décrit.

-   incrément

    Incrémentation entre les pointeurs successifs pendant une répétition.

-   nombre \_ de \_ pointeurs

    Nombre de pointeurs différents dans une instance de répétition.

-   Description du pointeur \_

    Description du pointeur.

Toutes les dispositions d’instance de pointeur utilisent l’instance de pointeur unique suivante \_<8> :

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

Voici les descripteurs d’instance :

**Instance unique d’un pointeur vers un type simple :**

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

**Pointeur de répétition fixe :**

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

**Pointeur de répétition de variable :**

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

Pour les instances de pointeurs REPEAT et variable à répétition fixe, il existe un ensemble de descriptions de décalage et de pointeur pour chaque pointeur de l’instance de répétition.

## <a name="pointers-layout-design-issues"></a>Problèmes de conception de la disposition des pointeurs

Cette section traite des problèmes liés au traitement des structures conformes et des pointeurs incorporés. Le problème est que le compilateur génère des dispositions de pointeur pour les structures et les tableaux avec une certaine redondance. Cela est avantageux, car les informations sont utiles et, par exemple, une structure conforme peut parcourir une disposition de pointeur pour traiter tous les pointeurs de la structure et du tableau conforme faisant partie de la structure conforme. Toutefois, il existe certaines situations incorporées qui nécessitent que le moteur de NDR effectue des tâches supplémentaires pour traiter toutes les dispositions de pointeur dans l’ordre approprié, en traitant chaque pointeur exactement une fois.

## <a name="what-the-compiler-generates"></a>Ce que le compilateur génère

Chaque objet abordé dans cette section a des pointeurs. par exemple, une structure conforme a des pointeurs dans la partie structure et dans les éléments du tableau. L’élément est une structure simple avec un pointeur.

1.  Structure conforme, niveau unique

    Le descripteur conforme a une partie PP dans laquelle tous les pointeurs sont décrits, à la fois à partir de la structure et à partir du tableau. La liste des membres a \_ une valeur FC à la place d’un pointeur. Le descripteur de tableau CARRAY possède des éléments via l’utilisation d’un complexe incorporé \_ et aucun descripteur de pointeur. L’élément a toujours son descripteur de pointeur unique. La disposition du pointeur précède la disposition des membres dans une structure conforme et des descripteurs de structure simples.

2.  Structure conforme, deux niveaux ou plus

    La description PP a des pointeurs de tous les niveaux. Elle réutilise la même description de tableau que la structure conforme interne. La liste des membres a \_ une valeur FC à la place d’un pointeur. Une structure incorporée est utilisée à l’aide d’un complexe incorporé. Le descripteur de structure conforme est réutilisé tel quel. La taille de la partie plate de la structure est également terminée, ce qui signifie que la taille de la structure de niveau supérieur inclut la taille plate de la structure incorporée.

3.  Structure complexe, niveau simple

    Les membres de pointeur sont marqués par un \_ pointeur FC. La disposition du pointeur est simplifiée de telle sorte qu’il existe un descripteur de pointeur (4 octets) pour chaque \_ entrée de pointeur FC de la liste. La disposition du pointeur est parcourue en parallèle avec un parcours de membre, autrement dit, un \_ pointeur FC provoque le traitement de la description suivante du pointeur. Le tableau CARRAY a une disposition de pointeur avec tous les descripteurs du tableau, puis l’élément, à l’aide d’un complexe incorporé. Le descripteur d’élément est réutilisé. La taille de la partie plate de la structure est terminée. en d’autres termes, la taille plate de la structure de niveau supérieur comprend la taille plate de la structure incorporée. La disposition des membres précède la disposition du pointeur pour les structures complexes.

    Par conséquent, la génération de description de tableau conforme est différente selon qu’il s’agit d’un tableau à l’intérieur d’une structure conforme ou à l’intérieur d’une structure complexe.

4.  Structure complexe, 2 niveaux ou plus, complexe en complexe

    La structure complexe de niveau supérieur a ses pointeurs membres, la structure complexe incorporée a ses pointeurs membres. Le descripteur de structure conforme est réutilisé. Le descripteur de tableau du haut est le tableau réutilisé à partir de la structure incorporée.

5.  Structure complexe avec une structure conforme incorporée

    Top = la structure conforme au niveau a ses pointeurs membres. Le descripteur de structure conforme est réutilisé tel quel. Le descripteur de tableau est réutilisé à partir de la structure conforme incorporée ; en d’autres termes, il n’a pas de pointeurs au niveau du descripteur de tableau. L’élément a son descripteur de pointeur.

6.  Tableaux de structures avec des pointeurs

    Un tableau de structures simples avec des pointeurs est généré sous la forme d’un SMFARRAY ou d’un CARRAY en fonction de la taille du tableau, mais dans les deux cas, il a une mise en forme de pointeur qui est terminée ( \_ répétition répétée ou variable \_ répétée). La disposition du pointeur précède la disposition des membres.

    Un tableau de structures complexes avec des pointeurs est généré sous la forme d’un tableau fictif, qu' \_ il soit fixe ou dimensionné, et dans les deux cas, n’a pas de disposition de pointeur.

## <a name="what-the-ndr-engine-does"></a>Ce que fait le moteur de NDR

Cette section décrit le comportement du moteur de rapport de non-remise.

**Passe de marshaling**

1.  Structures conformes et structure conforme incorporée.

    La structure de niveau supérieur se comporte comme une structure à un seul niveau.

2.  Structure complexe incorporée avec tableau conforme

    Toute structure complexe force la structure externe à être une structure complexe. La structure incorporée ne marshale jamais son tableau. Chaque structure passe toujours par des pointeurs incorporés en marshalant simplement les membres et un membre qui se trouve comme un \_ pointeur FC.

3.  Structure complexe avec une structure conforme

    La structure conforme incorporée la plus haute marshale le tableau conforme et tous les pointeurs. Le moteur de rapport de non-remise ne descend jamais des structures conformes imbriquées, le cas échéant ; Cela simplifie la solution, car une structure conforme est un objet feuille en ce qui concerne le marshaling des objets incorporés. La structure complexe de niveau supérieur ignore le marshaling de tableau.

**Démarshaling, bufsizing et libération des passes**

Le démarshaling est symétrique au marshaling ; la première opération effectuée pour les structures complexes consiste à Rechercher l’emplacement des pointeurs dans la mémoire tampon au moyen d’appeler la fonction **NdrComplexStructBufferSize** . Il démarshale ensuite les pointeurs en parallèle, ce qui permet d’utiliser le même schéma pour démarshaler correctement les pointeurs. Il ne doit y avoir aucune confusion en ce qui concerne les objets dimensionnés et les unions. l’image mémoire ne doit pas être utilisée pour les objets dimensionnés et les unions, uniquement pour le contenu de la mémoire tampon.

Les indicateurs utilisés pour effectuer correctement le marshaling et le démarshaling sont utilisés de la même façon dans bufsizing et pour s’assurer que les pointeurs sont parcourus une seule fois.

**Passe de primauté des itérations**

Au premier abord, le passage d’un niveau d’enprimautément est un peu semblable au marshaling/démarshaling. deux tests sont requis pour traiter des structures complexes. La première passe convertit la partie plate et recherche l’emplacement des pointeurs dans la mémoire tampon, de la même façon que bufsizing effectue cette opération pour démarshaler. La deuxième passe convertit ensuite les pointeurs.

Les passes d’un niveau d’inversion varient selon la méthode suivante : chaque structure et chaque membre doivent faire l’élément d’un pas à pas jusqu’à ce que le membre feuille ou l’élément soit un type simple. Cela diffère du démarshaling ; dans le démarshaling, par exemple, il n’est jamais nécessaire de traiter les structures conformes incorporées dans les structures conformes, ou tout membre de la structure conforme, pour cette question. Un autre problème est que la conversion n’est pas une opération idempotent. par conséquent, le démarshaling peut rétablir le démarshaling de certains morceaux sans nuire, tandis que la conversion doit être effectuée sur une base strictement unique par type.

Par conséquent, l’algorithme de primauté des valeurs peut être résumé comme suit. Le rapport de non-remise a une notion de la structure conforme de niveau supérieur et un indicateur pour marquer cela, le cas échéant. Lorsque vous parcourez la première fois, par exemple pour convertir la partie plate et obtenir l’emplacement des pointeurs, cette notion n’est pas utilisée. Le rapport de non-remise dépasserait les parties plates de tous les niveaux de structures et n’interviendra jamais dans le traitement des pointeurs. Enfin, NDR convertit le tableau au niveau supérieur.

Lorsque vous parcourez la deuxième fois, l’indicateur est utilisé pour marquer la passe du pointeur incorporé afin d’éviter d’entrer des niveaux plus détaillés des structures conformes, puis de la structure conforme la plus haute. De cette façon, l’indicateur force le comportement de marshaling/démarshaling commun, ce qui évite d’avoir à décroisser les niveaux des structures conformes.

La deuxième passe pour les structures complexes avec des tableaux conformes fonctionne comme suit : les structures complexes fonctionnent de la manière courante. ce qui signifie que les niveaux les plus approfondis ne verront jamais ou ignorent leur taille conforme ou leurs tableaux conformes, et préfèrent simplement parcourir leurs membres sans toucher au tableau.

Pour les structures complexes avec des structures conformes, la structure conforme doit savoir s’il s’agit d’un niveau supérieur et s’il est dans une structure complexe. La partie plate du tableau est traitée par la structure conforme la plus haute. À la deuxième passe, la structure conforme la plus haute ignore la partie plate et passe par la disposition du pointeur et retourne. La structure supérieure la plus complexe ignore sa partie plate et ignore également la disposition du pointeur.

**L’aspect robuste des parcours de primauté des niveaux de l’élément**

L’ordre de primauté des erreurs de l’ordre de primauté vérifie les conditions de mémoire tampon inhabituelles et effectue d’autres vérifications de nature non corrélée. Les vérifications destinées à des valeurs corrélées (telles que l’argument de dimensionnement et la taille conforme) ne peuvent pas être effectuées à l’aide de cette étape. ils sont exécutés plus tard, lors de l’démarshaling.

 

 




