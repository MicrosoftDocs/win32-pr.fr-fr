---
title: Type simple HexInt64Type
description: Définit un type hexadécimal sur 8 octets. | Type simple HexInt64Type
ms.assetid: 2e81ec2b-cf67-42df-92a0-bf45b6dca051
keywords:
- Journal des types simples HexInt64Type
topic_type:
- apiref
api_name:
- HexInt64Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 22b0cacc482f5bde657c9cf5eb451acb273e79cda0cbf14a4d3536fe90af756c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652419"
---
# <a name="hexint64type-simple-type"></a>Type simple HexInt64Type

Définit un type hexadécimal sur 8 octets.

``` syntax
<xs:simpleType name="HexInt64Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,16}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **HexInt64Type** est une [chaîne](/dotnet/api/system.string) qui est limitée par le modèle suivant :

-   `0[xX][0-9A-Fa-f]{1,16}`

    La valeur peut contenir entre un et seize caractères hexadécimaux (par exemple, 0xA ou 0xac7bd361004fe190).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

