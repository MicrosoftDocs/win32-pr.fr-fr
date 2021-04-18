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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542984"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 




