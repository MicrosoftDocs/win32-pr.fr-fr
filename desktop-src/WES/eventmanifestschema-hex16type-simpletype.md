---
title: Type simple HexInt16Type
description: Définit un type hexadécimal sur 2 octets.
ms.assetid: d33d24e7-d260-49ea-a8ba-187b9b7a3a9c
keywords:
- Journal des types simples HexInt16Type
topic_type:
- apiref
api_name:
- HexInt16Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5f441071daa84f162a1dacbd16513fe2550b99d34d24ed90205ff4d8d184493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055958"
---
# <a name="hexint16type-simple-type"></a>Type simple HexInt16Type

Définit un type hexadécimal sur 2 octets.

``` syntax
<xs:simpleType name="HexInt16Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,4}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **HexInt16Type** est une **chaîne** qui est limitée par le modèle suivant :

-   `0[xX][0-9A-Fa-f]{1,4}`

    La valeur peut contenir de un à quatre caractères hexadécimaux (par exemple, 0xA ou 0xac7b).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





