---
description: Contient le nom ou la description d’un profil de réseau local sans fil.
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: Type simple nameType (LAN_policy) (profil)
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
ms.openlocfilehash: 9179efbb52a07983f8d40c271ffc5c0b4ab3eea0c7ddd3a73e1ba790f867143f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683999"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a>Type simple nameType (LAN_policy) pour profileschema

Le type simple nameType peut contenir le nom ou une description d’un profil de réseau local sans fil. Cette valeur de chaîne doit être comprise entre 1 et 255 caractères.

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
|-------------------------------------|---------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                |
| Composant redistribuable<br/>          | API de réseau local sans fil pour Windows XP avec SP2<br/>                 |



 

 




