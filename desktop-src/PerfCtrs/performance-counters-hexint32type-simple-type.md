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
ms.openlocfilehash: 08b9ea7e483f6580e3f896a6a3f54a65e9117597538564889df8a5afb2fe795f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033479"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




