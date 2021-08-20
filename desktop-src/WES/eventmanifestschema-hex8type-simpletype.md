---
title: Type simple HexInt8Type
description: Définit un type hexadécimal sur 1 octet.
ms.assetid: 390acf84-7b5c-45e7-83bd-9f3115099568
keywords:
- Journal des types simples HexInt8Type
topic_type:
- apiref
api_name:
- HexInt8Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d2d70b7258317f16ac4e134f011a85218fa1b63aa768136f68b1d21c901856e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121005"
---
# <a name="hexint8type-simple-type"></a>Type simple HexInt8Type

Définit un type hexadécimal sur 1 octet.

``` syntax
<xs:simpleType name="HexInt8Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,2}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **HexInt8Type** est une [chaîne](/dotnet/api/system.string) qui est limitée par le modèle suivant :

-   `0[xX][0-9A-Fa-f]{1,2}`

    La valeur peut contenir de un à deux caractères hexadécimaux (par exemple, 0xA ou 0xac).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

