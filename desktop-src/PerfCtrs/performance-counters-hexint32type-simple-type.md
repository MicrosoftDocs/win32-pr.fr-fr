---
description: Définit un type hexadécimal sur 4 octets.
ms.assetid: d0e538c1-f22e-4905-ba73-b670fa7eb174
title: Type simple HexInt32Type (compteurs de performance)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d2392f2240ca9ca61525b27993e16bcab979a97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127218396"
---
# <a name="hexint32type-simple-type-performance-counters"></a>Type simple HexInt32Type (compteurs de performance)

Définit un type hexadécimal sur 4 octets.

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **HexInt32Type** est un **XS : String** qui est limité par le modèle suivant :

-   `0[xX][0-9A-Fa-f]{1,8}`

    La valeur peut contenir de un à huit caractères hexadécimaux (par exemple, 0xA ou 0xac7bd361).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




