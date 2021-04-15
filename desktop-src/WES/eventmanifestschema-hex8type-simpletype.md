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
ms.openlocfilehash: e68e56340ee535531fb6711dcf01a72d92665cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466966"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

