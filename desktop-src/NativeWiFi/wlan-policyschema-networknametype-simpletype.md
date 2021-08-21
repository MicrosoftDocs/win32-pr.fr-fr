---
description: Définit un type de chaîne pour les identificateurs de jeu de service (SSID).
ms.assetid: c9e79a3d-7d5c-4320-ade2-40124de00920
title: Type simple networkNameType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkNameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8f653c84f36730ed9f6f078b3713dde414fbf63469bd4ea43f632842d33d7e14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064749"
---
# <a name="networknametype-simple-type"></a>Type simple networkNameType

Le type simple networkNameType définit un type de chaîne pour les identificateurs de jeu de service (SSID). Un SSID est une chaîne d’au moins un caractère et de 32 caractères au maximum.

``` syntax
<xs:simpleType name="networkNameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="32"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




