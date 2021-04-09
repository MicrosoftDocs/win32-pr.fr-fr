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
ms.openlocfilehash: c3c776bbd721bbb03b4f5549f87d48248a35206b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033959"
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
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                         |



 

 




