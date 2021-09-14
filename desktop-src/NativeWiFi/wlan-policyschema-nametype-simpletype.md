---
description: Définit un type de chaîne pour le nom ou la description d’un profil de stratégie de réseau local sans fil.
ms.assetid: a01e8789-3401-4e58-b733-2ec95fc895b6
title: Type simple nameType (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8a2c0bdf281e27ba7a85271fe7777076ada9ff2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110446"
---
# <a name="nametype-simple-type-lan_policy"></a>Type simple nameType (LAN_policy)

Le type simple nameType définit un type de chaîne pour le nom ou la description d’un profil de stratégie de réseau local sans fil. Les noms et les descriptions sont des chaînes d’au moins un caractère et de 255 caractères de long.

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




