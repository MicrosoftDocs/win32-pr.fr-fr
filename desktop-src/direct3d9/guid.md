---
description: Définit un GUID qui peut être utilisé dans d’autres modèles.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: Guid (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521431"
---
# <a name="guid-directx-9"></a>Guid (DirectX 9)

Définit un GUID qui peut être utilisé dans d’autres modèles.

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

Où les paramètres forment le format de stockage binaire pour un GUID :

-   données1-valeur de données de l’entier non signé 32 bits
-   data2-valeur de données de l’entier non signé 16 bits
-   data3-valeur de données de l’entier non signé 16 bits
-   data4-un tableau de caractères non signés

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



