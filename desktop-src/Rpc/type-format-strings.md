---
title: Chaînes de format de type
description: Les caractères de format dénotent les objets qui intéressent le moteur de NDR.
ms.assetid: 71117082-07b0-4ba4-a920-09be8d8427ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618d857e487f86e2d28ed18300d82e94b76e3a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011395"
---
# <a name="type-format-strings"></a>Chaînes de format de type

Les caractères de format dénotent les objets qui intéressent le moteur de NDR. Il existe un caractère de format pour chaque type de base, pour divers types complexes et pour les descriptions des pointeurs, de l’empaquetage, de l’alignement et d’autres objets divers. Pour les types composés, plusieurs catégories de structures et de tableaux sont reconnues en fonction de leurs propriétés de performances. Une chaîne de format pour chaque catégorie commence par un jeton FC identifiant la chaîne de format particulière. Les caractères de format pour les structures et les catégories de tableaux peuvent partager les correctifs dans le nom du jeton FC de début indiqué dans le tableau suivant.



| Caractère de format | Description                                    |
|------------------|------------------------------------------------|
| C                | Indique des informations de conformité dans le type. |
| V                | Indique les informations de variance dans le type.    |
| P                | Indique que les pointeurs font partie du type.     |



 

Par exemple, FC \_ CSTRUCT et FC \_ CARRAY identifient la structure conforme et les descripteurs de tableau conformes, respectivement.

Les caractères de format suivants sont des significations spéciales.



| Caractère de format | Description                                                                         |
|------------------|-------------------------------------------------------------------------------------|
| FC \_ pp           | Indique le début de la section de description du pointeur d’une structure ou d’un tableau. |



 

Les chaînes de format de type NDR RPC sont décrites plus en détail dans les rubriques suivantes :

-   [Types simples](simple-types-tfs.md)
-   [Pointeurs](pointers-tfs.md)
-   [Tableaux](arrays-tfs.md)
-   [Chaînes](strings-tfs.md)
-   [Descripteurs de corrélation](correlation-descriptors-tfs.md)
-   [Structures](structures-tfs.md)
-   [Disposition du pointeur](pointer-layout-tfs.md)
-   [Unions](unions-tfs.md)
-   [Transmettre \_ en tant que et représenter \_ comme](transmit-as-and-represent-as-tfs.md)
-   [Marshal d’utilisateur](user-marshal-tfs.md)

 

 




