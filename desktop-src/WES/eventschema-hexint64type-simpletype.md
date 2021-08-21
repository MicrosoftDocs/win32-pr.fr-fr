---
title: Type simple HexInt64Type (schéma d’événement)
description: Définit un type hexadécimal sur 8 octets. | Type simple HexInt64Type (schéma d’événement)
ms.assetid: b4d8f416-d9e3-4a07-9b08-6f634c0de06c
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
ms.openlocfilehash: 1fcc4e3cea12be0fecaf7cef2dcd6f9687f4aa4340f9eaca4f8a6bad10c88eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120144"
---
# <a name="hexint64type-simple-type-event-schema"></a>Type simple HexInt64Type (schéma d’événement)

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

Le type simple **HexInt64Type** est une **chaîne** qui est limitée par le modèle suivant :

-   `0[xX][0-9A-Fa-f]{1,16}`

    La valeur peut contenir entre un et seize caractères hexadécimaux (par exemple, 0xA ou 0xac7bd361004fe190).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





