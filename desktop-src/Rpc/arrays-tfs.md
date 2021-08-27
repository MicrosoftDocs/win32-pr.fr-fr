---
title: Tableaux (RPC) (TFS)
description: Les catégories de tableau de l’appel de procédure distante (RPC) incluent des catégories de taille fixe, de conformité et de variation, variables et complexes.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6271f6a459ebfb96cc5c4d55153bb4c77b013a50925d9c3a4ba9dd81b0f6fbdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073489"
---
# <a name="arrays-rpc"></a>Tableaux (RPC)

Plusieurs catégories de tableaux ont été définies en fonction de leurs caractéristiques de performances, en particulier si le tableau peut être copié par bloc.

Pour certaines catégories, telles qu’un tableau de taille fixe, il existe deux types de descripteurs de tableau ; ils sont indiqués par un correctif dans le nom du jeton FC de début.



| Caractère de format | Description                                                           |
|------------------|-----------------------------------------------------------------------|
| SM               | La taille totale du type peut être représentée dans un entier non signé 16 bits.    |
| LG               | La taille totale du type a besoin d’un long non signé 32 bits pour être représenté. |



 

Champs communs aux tableaux :

-   \_taille totale

    Taille totale du tableau en mémoire, en octets. Cela est identique à la taille du câble après l’alignement. La taille totale est calculée pour les catégories pour lesquelles le problème de remplissage n’existe pas et la taille correspond à la taille réelle du tableau.

-   taille de l’élément \_

    Taille totale en mémoire d’un seul élément du tableau, y compris le remplissage (cela peut se produire pour les tableaux complexes uniquement).

-   Description de l’élément \_

    Description du type d’élément de tableau.

-   disposition du pointeur \_

    Pour plus d’informations, consultez la rubrique [disposition du pointeur](pointer-layout-tfs.md) .

## <a name="fixed-sized-arrays"></a>Tableaux de taille fixe

Une chaîne de format de tableau de taille fixe est générée pour les tableaux qui ont une taille connue et, par conséquent, peut être copiée par bloc dans la mémoire tampon de marshaling. Les deux formats de descripteur de tableau fixes sont les suivants.

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

et

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a>Tableau conforme

Un tableau conforme peut être copié par bloc une fois que la taille du tableau est connue.

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

La description de la conformité \_<> est un descripteur de corrélation et contient 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non.

## <a name="conformant-varying-array"></a>Tableau variable conforme

Un tableau à variation conforme peut également être copié par bloc.

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

La description de la conformité \_<> et la description de la variance \_<> est un descripteur de corrélation et a 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non.

## <a name="varying-array"></a>Tableau variable

Les tableaux variables ont deux possibilités en fonction de la taille du tableau.

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

La description de l’écart \_<> est un descripteur de corrélation et a 4 ou 6 octets selon le [**/Robust**](/windows/desktop/Midl/-robust) utilisé.

Pour les tableaux de variables incorporés à l’intérieur d’une structure, le champ décalage<2> de la description de l’écart \_<> est un décalage relatif de la position du tableau variable dans la structure à l’écart qui décrit le champ. Le décalage est généralement relatif au début de la structure.

## <a name="complex-arrays"></a>Tableaux complexes

Un tableau complexe est un tableau avec un élément qui l’empêche d’être copié par bloc, et par conséquent, une action supplémentaire doit être effectuée. Ces éléments rendent un tableau complexe :

-   types simples : ENUM16, \_ \_ INT3264 (sur les plateformes 64 bits uniquement), un intégral avec \[ [ **Range**](/windows/desktop/Midl/range)\]
-   pointeurs d’interface et de référence (tous les pointeurs sur les plateformes 64 bits)
-   unions
-   structures complexes (consultez la rubrique Description de la structure complexe pour obtenir une liste complète des raisons pour lesquelles une structure est complexe)
-   éléments définis avec \[ [**transmit \_ As**](/windows/desktop/Midl/transmit-as) \] , \[ [**\_ Marshal d’utilisateur**](/windows/desktop/Midl/user-marshal)\]
-   Tous les tableaux multidimensionnels avec au moins une dimension en conformité et/ou variable sont complexes, quel que soit le type d’élément sous-jacent.

La description du tableau complexe est la suivante :

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

Le nombre \_ d' \_ éléments<2> champ est zéro si le tableau est conforme.

La description de la conformité \_<> et la description de la variance \_<> est un descripteur de corrélation et a 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non. Si le tableau est conforme et/ou variance, la description de la conformité \_<> et/ou la description de la variance \_<> champ (s) ont des descriptions valides, sinon les 4 premiers octets du descripteur de corrélation sont définis sur 0xFFFFFFFF. Les indicateurs, le cas échéant, sont définis sur zéro.

 

 
