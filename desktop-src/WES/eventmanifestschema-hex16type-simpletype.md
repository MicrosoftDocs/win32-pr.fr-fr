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
ms.openlocfilehash: 6aaa5021fbc5a7de5c16083c0f7744bc4a154c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466606"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





