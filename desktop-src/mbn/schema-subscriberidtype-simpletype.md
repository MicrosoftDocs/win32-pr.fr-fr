---
description: Définit un type pour l’élément abonné du profil haut débit mobile.
ms.assetid: b36df4d3-f558-4af8-8f63-e4991c34990f
title: Type simple subscriberIdType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- subscriberIdType
api_type:
- Schema
ms.openlocfilehash: aac83be84ae313f572d82e6b4c9a2afb14beeb7e15c531eaae7efd67bcc90464
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881363"
---
# <a name="subscriberidtype-simple-type"></a>Type simple subscriberIdType

Le type simple **subscriberIdType** définit un type pour l’élément [**abonné**](schema-subscriberid-mbnprofile-element.md) du profil haut débit mobile. Ce type est une collection d’un ou de plusieurs caractères.

``` syntax
<xs:simpleType name="subscriberIdType">
    <xs:restriction
        base="token"
    >
        <xs:minLength
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




