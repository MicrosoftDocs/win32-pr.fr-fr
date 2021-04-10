---
title: Structures (RPC)
description: Description de différents types de structures dans l’appel de procédure distante (RPC).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031585"
---
# <a name="structures-rpc"></a>Structures (RPC)

Il existe plusieurs catégories de structures, progressivement plus compliquées en termes d’actions requises pour le marshaling. Ils commencent par une structure simple qui peut être copiée par bloc dans son ensemble et qui continuent à une structure complexe qui doit être un champ de champ par champ.

-   [Structure simple](#simple-structure)
-   [Structure simple avec pointeurs](#simple-structure-with-pointers)
-   [Structure conforme](#conformant-structure)
-   [Structure conforme avec des pointeurs](#conformant-structure-with-pointers)
-   [Structure variable conforme (avec ou sans pointeurs)](#conformant-varying-structure-with-or-without-pointers)
-   [Structure matérielle](#hard-structure)
-   [Structure complexe](#complex-structure)
-   [Description de la disposition des membres de la structure](#structure-member-layout-description)

> [!Note]  
> En comparaison avec les catégories de tableau, il devient clair que seules les structures jusqu’à 64 Ko peuvent être décrites (la taille est pour la partie plate de la structure), il n’y a pas d’équivalent des tableaux SM et LG.

 

**Membres communs aux structures**

-   **repère**

    L’alignement nécessaire de la mémoire tampon avant d’unmarshaler la structure. Les valeurs valides sont 0, 1, 3 et 7 (l’alignement réel moins 1).

-   **taille de la mémoire \_**

    Taille de la structure en octets dans la mémoire ; pour les structures conformes, cette taille n’inclut pas la taille du tableau.

-   **\_Description du décalage par rapport au \_ tableau \_**

    Offset du pointeur de chaîne de format actuel vers la description du tableau conforme contenu dans une structure.

-   **disposition des membres \_**

    Description de chaque élément de la structure. Les routines de NDR doivent uniquement examiner cette partie de la chaîne de format d’un type si la transformation endian est nécessaire ou si le type est une structure complexe.

-   **disposition du pointeur \_**

    Consultez la section [disposition du pointeur](pointer-layout-tfs.md) .

## <a name="simple-structure"></a>Structure simple

Une structure simple contient uniquement des types de base, des tableaux fixes et d’autres structures simples. La principale fonctionnalité de la structure simple est qu’elle peut être copiée par bloc dans son ensemble.

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a>Structure simple avec pointeurs

Une structure simple avec des pointeurs contient uniquement des types de base, des pointeurs, des tableaux fixes, des structures simples et d’autres structures simples avec des pointeurs. Étant donné que la<> de disposition ne doit être visitée que lors d’une conversion d’un niveau d’enprimautément, elle est placée à la fin de la description.

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a>Structure conforme

Une structure conforme contient uniquement des types de base, des tableaux fixes et des structures simples, et doit contenir une chaîne conforme ou un tableau conforme. Ce tableau peut en fait être contenu dans une autre structure conforme ou une structure conforme avec des pointeurs qui est incorporé dans cette structure.

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a>Structure conforme avec des pointeurs

Une structure conforme avec des pointeurs contient uniquement des types de base, des pointeurs, des tableaux fixes, des structures simples et des structures simples avec des pointeurs ; une structure conforme doit contenir un tableau conforme. Ce tableau peut en fait être contenu dans une autre structure conforme ou une structure conforme avec des pointeurs incorporés dans cette structure.

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a>Structure variable conforme (avec ou sans pointeurs)

Une structure variable conforme contient uniquement des types simples, des pointeurs, des tableaux fixes, des structures simples et des structures simples avec des pointeurs. une structure variable conforme doit contenir soit une chaîne conforme soit un tableau à variation conforme. La chaîne ou le tableau conforme peut en fait être contenu dans une autre structure conforme ou une structure conforme avec des pointeurs incorporés dans cette structure.

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a>Structure matérielle

La structure matérielle était un concept visant à éliminer des pénalités en matière de traitement de structures complexes. Elle est dérivée d’une observation qu’une structure complexe n’a généralement qu’une ou deux conditions qui empêchent la copie de blocs et, par conséquent, de altérer ses performances par rapport à une structure simple. Les coupable sont généralement des unions ou des champs d’énumération.

Une structure matérielle est une structure qui a un enum16, un remplissage de fin en mémoire ou une Union comme dernier membre. Ces trois éléments empêchent la structure de tomber dans l’une des catégories de structures précédentes, qui profitent de la surcharge d’interprétation et du potentiel d’optimisation maximal, mais ne la forcent pas à la catégorie de structure complexe la plus coûteuse.

Le enum16 ne doit pas provoquer la différence entre la mémoire et la taille des câbles de la structure. La structure ne peut pas avoir de tableau conforme, ni de pointeurs (sauf une partie de l’Union); les seuls autres membres autorisés sont les types de base, les tableaux fixes et les structures simples.

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

Le champ décalage de l’énumération \_<2> fournit l’offset du début de la structure en mémoire à un enum16 si celui-ci en contient un ; sinon, le \_ décalage enum<2> champ est – 1.

Le \_ champ Taille de copie<2> fournit le nombre total d’octets dans la structure, qui peuvent être copiés par blocs dans/à partir de la mémoire tampon. Ce total n’inclut pas d’Union de fin ni de remplissage de fin dans la mémoire. Cette valeur est également la quantité que le pointeur de mémoire tampon doit être incrémenté à la suite de la copie.

Le \_ \_ champ de> de copie de mem<2 est le nombre d’octets que le pointeur de mémoire doit être incrémenté à la suite de la copie de bloc avant toute Union de fin. L’incrémentation de cette quantité (et non de la taille de copie \_<2 octets>) produit un pointeur de mémoire approprié à toute Union de fin.

## <a name="complex-structure"></a>Structure complexe

Une structure complexe est une structure qui contient un ou plusieurs champs qui empêchent la structure d’être copiée par bloc ou pour lesquels une vérification supplémentaire doit être effectuée pendant le marshaling ou le démarshaling (par exemple, des contrôles liés sur une énumération). Les types de NDR suivants appartiennent à cette catégorie :

-   [types simples](simple-types-tfs.md): ENUM16, \_ \_ INT3264 (sur les plateformes 64 bits uniquement), un intégral avec \[ [ **Range**](/windows/desktop/Midl/range)\]
-   remplissage de l’alignement à la fin de la structure
-   pointeurs d’interface (ils utilisent un complexe intégré)
-   pointeurs ignorés (associés à l' \[ attribut [**ignore**](/windows/desktop/Midl/ignore) \] et au jeton FC ignoré \_ )
-   tableaux complexes, tableaux variables, tableaux de chaînes
-   tableaux conformes multidimensionnels avec au moins une dimension fixe
-   unions
-   éléments définis avec \[ [**transmettre \_ en tant que**](/windows/desktop/Midl/transmit-as) \] , \[ [**représenter \_ comme**](/windows/desktop/Midl/represent-as) \] , \[ [**\_ marshaleur de câble**](/windows/desktop/Midl/wire-marshal) \] , \[ [**\_ Marshal d’utilisateur**](/windows/desktop/Midl/user-marshal)\]
-   structures complexes incorporées
-   remplissage à la fin de la structure

Une structure complexe a la description de format suivante :

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

La \_ taille de la mémoire<2> champ est la taille de la structure en mémoire, en octets.

Si la structure contient un tableau conforme, le \_ champ offset to \_ conformed \_ array \_ Description<2> champ fournit le décalage à la description du tableau conforme, sinon il est égal à zéro.

Si la structure a des pointeurs, le décalage \_ vers la \_ disposition du pointeur \_<2> champ fournit le décalage au-delà de la disposition de la structure jusqu’à la disposition du pointeur, sinon ce champ est égal à zéro.

La disposition du pointeur \_<> champ d’une structure complexe est gérée de façon légèrement différente de celle des autres structures. La disposition du pointeur \_<> champ d’une structure complexe contient uniquement les descriptions des champs de pointeur réels de la structure elle-même. Tous les pointeurs contenus dans des tableaux, unions ou structures incorporés ne sont pas décrits dans le champ disposition du pointeur de la structure complexe \_<> .

> [!Note]  
> Cela s’oppose à d’autres structures, qui dupliquent la description de tous les pointeurs contenus dans les tableaux ou les structures incorporés dans leur propre disposition de pointeur \_<> champ également.

 

Le format de la disposition du pointeur d’une structure complexe est également radicalement différent. Étant donné qu’il contient uniquement des descriptions des membres de pointeur réels et qu’une structure complexe est marshalée et démarshalée un champ à la fois, le champ de disposition du pointeur \_<> contient simplement la description du pointeur de tous les membres du pointeur. Il n’y a pas \_ de point de départ pour le premier plan et aucune des informations de disposition du pointeur habituelle n' \_<> .

## <a name="structure-member-layout-description"></a>Description de la disposition des membres de la structure

La description de la disposition d’une structure contient un ou plusieurs des caractères de format suivants :

-   N’importe quel caractère de type de base, comme FC \_ Char, etc.
-   Directives d’alignement. Trois caractères de format spécifient l’alignement du pointeur de mémoire : FC \_ ALIGNM2, FC \_ ALIGNM4 et FC \_ ALIGNM8.
    > [!Note]  
    > Il existe également des jetons d’alignement de la mémoire tampon, FC \_ ALIGNB2 via FC \_ ALIGNM8 ; ceux-ci ne sont pas utilisés.

     

-   Remplissage de la mémoire. Elles se produisent uniquement à la fin de la description d’une structure et désignent le nombre d’octets de remplissage dans la mémoire avant le tableau conforme dans la structure : FC \_ STRUCTPADn, où n est le nombre d’octets de remplissage.
-   Tout type non de base incorporé (Notez, toutefois, qu’un tableau conforme ne se produit jamais dans la disposition de la structure). Il comporte une description de 4 octets :

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    où l’alignement sur deux octets n’est pas garanti pour l’offset.

    \_le bloc de mémoire<1> est un remplissage requis en mémoire avant le champ complexe.

    décalage \_ vers \_ la description<2> est un décalage de type relatif par rapport au type incorporé.

Il peut également y avoir un \_ tampon FC avant l’arrêt de la solution FC, \_ si nécessaire, pour s’assurer que la chaîne de format sera alignée sur une limite de 2 octets à la suite de l' \_ extrémité FC.

 

 