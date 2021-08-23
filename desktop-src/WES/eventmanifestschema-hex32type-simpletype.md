---
title: Type simple HexInt32Type (schéma EventManifest)
description: Définit un type hexadécimal sur 4 octets. | Type simple HexInt32Type (schéma EventManifest)
ms.assetid: b1006593-c6f2-4669-b242-758ce9977565
keywords:
- Journal des types simples HexInt32Type
topic_type:
- apiref
api_name:
- HexInt32Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c78a101ec9854b8820b7c9170ea43f06258528de9fdc9d4b02bb41945ba3a7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248099"
---
# <a name="hexint32type-simple-type-eventmanifest-schema"></a>Type simple HexInt32Type (schéma EventManifest)

Définit un type hexadécimal sur 4 octets.

``` syntax
<xs:simpleType name="HexInt32Type">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="0[xX][0-9A-Fa-f]{1,8}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modèles

Le type simple **HexInt32Type** est une **chaîne** qui est limitée par le modèle suivant :

-   `0[xX][0-9A-Fa-f]{1,8}`

    La valeur peut contenir de un à huit caractères hexadécimaux (par exemple, 0xA ou 0xac7bd361).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





