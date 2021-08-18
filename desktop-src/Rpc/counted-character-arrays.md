---
title: Tableaux de caractères comptés
description: L’attribut \ size \_ is \ indique la limite supérieure du tableau, tandis que l' \_ attribut \ length est \ indique le nombre d’éléments de tableau à transmettre.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8abb7a391c617cadae5af396c4b4216dc9d14abf0f6d31ead3a6e075c7357b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931128"
---
# <a name="counted-character-arrays"></a>Tableaux de caractères comptés

L' \[ attribut [size \_ is](/windows/desktop/Midl/size-is) \] indique la limite supérieure du tableau, tandis que la \[ [longueur \_ est](/windows/desktop/Midl/length-is) \] attribute indique le nombre d’éléments de tableau à transmettre. En plus du tableau, le prototype de procédure distante doit inclure toutes les variables représentant la longueur ou la taille qui déterminent les éléments du tableau transmis (ils peuvent être des paramètres distincts ou regroupés avec la chaîne dans une structure). Ces attributs peuvent être utilisés avec des tableaux de caractères à caractères larges ou codés sur un octet de la même manière qu’avec des tableaux d’autres types.

Les informations contenues dans cette section décrivent les prototypes de paramètres de procédure distante pour les tableaux de caractères. Elle est composée des rubriques suivantes :

-   [\[in, out, la taille \_ est un \] prototype](-in-out-size-is-prototype.md)
-   [\[dans, la taille \_ est et sortante, la taille \_ est un \] prototype](-in-size-is-and-out-size-is-prototype.md)

 

 