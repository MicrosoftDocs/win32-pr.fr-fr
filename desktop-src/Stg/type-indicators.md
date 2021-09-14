---
title: Indicateurs de type
description: Les propriétés réelles suivent la table des valeurs de jeu de propriétés d’identificateurs de propriété/de paires de décalage. Chaque propriété est stockée sous la forme d’un DWORD, suivi de la valeur du type de données.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237221"
---
# <a name="type-indicators"></a>Indicateurs de type

Les propriétés réelles suivent la table des valeurs de jeu de propriétés d’identificateurs de propriété/de paires de décalage. Chaque propriété est stockée sous la forme d’un **DWORD**, suivi de la valeur du type de données.

Les indicateurs de type et leurs valeurs associées sont décrits dans la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Toutes les paires type/valeur doivent commencer sur une limite de 32 bits. Par conséquent, les valeurs peuvent être suivies avec des octets null pour aligner la paire suivante sur une limite de 32 bits.

L’exemple de code suivant calcule le nombre d’octets requis pour l’alignement sur une limite de 32 bits, en fonction d’un nombre d’octets.


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



Dans un vecteur de valeurs, chaque répétition d’une valeur scalaire simple inférieure à 32 bits doit être alignée avec son alignement naturel plutôt qu’avec un alignement de 32 bits. Dans la pratique, cela n’est significatif que pour les types **VT \_ UI1**, **VT \_ UI2**, **VT \_ I2** et **VT \_ bool** (qui ont un alignement naturel sur un octet ou sur deux octets). Tous les autres types ont un alignement naturel sur quatre octets. Certains types, par exemple, **VT \_ R8**, ont en fait un alignement naturel sur 8 octets, mais ils sont stockés comme s’ils avaient un alignement sur quatre octets.

Une valeur de propriété avec l’indicateur de type **VT \_ I2** \| **VT \_ Vector** contient les éléments suivants :

-   Nombre d’éléments **DWORD** .
-   Séquence d’entiers compactés sur deux octets sans remplissage null entre eux.

> [!IMPORTANT]
> Tout nombre 32 bits ou type de propriété qui sont stockés dans le cadre d’un élément de propriété Vector doit également être aligné sur 32 bits.

 

Une valeur de propriété de type identificateur **VT \_ LPSTR** VT \| **\_ vecteur** inclut les éléments suivants :

-   Nombre d’éléments **DWORD** (**DWORD** *cElems*).
-   Séquence de chaînes (**char** *RGCH \[ \]*), chacune précédée d’un **DWORD** de longueur-nombre et éventuellement suivie d’un remplissage null pour arrondir à une limite de 32 bits.

 

 