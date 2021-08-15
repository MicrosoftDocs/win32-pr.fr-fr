---
description: Définit un type de chaîne pour le nom ou la description d’un profil de stratégie de réseau local câblé.
ms.assetid: 89de1e7a-618d-4501-a134-c7a37f9c552d
title: type simple nameType (LAN_policy)
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
ms.openlocfilehash: 3b3d558717777c9b2bead2fd7e141dee38b22491af4142d4948c7f1f76aadfd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065109"
---
# <a name="nametype-simple-type-lan_policy"></a>type simple nameType (LAN_policy)

Le type simple nameType définit un type de chaîne pour le nom ou la description d’un profil de stratégie de réseau local câblé. Les noms et les descriptions sont des chaînes d’au moins un caractère et de 255 caractères de long.

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




