---
title: Type simple LengthType
description: Définit un type de longueur utilisé pour spécifier le nombre d’octets ou de caractères dans un élément de données de longueur variable, tel que des données binaires ou une chaîne ANSI ou Unicode.
ms.assetid: a15e4241-cce3-4f62-bc1c-f70fb1ea5d38
keywords:
- Journal des types simples LengthType
topic_type:
- apiref
api_name:
- LengthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9ded861e3e46cd5e4fc6c069d95bba9f0ab3457559bf319aef41cdf906e193b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997859"
---
# <a name="lengthtype-simple-type"></a>Type simple LengthType

Définit un type de longueur utilisé pour spécifier le nombre d’octets ou de caractères dans un élément de données de longueur variable, tel que des données binaires ou une chaîne ANSI ou Unicode. La valeur peut être spécifiée en tant que valeur XS : unsignedShort ou en tant que chaîne qui fait référence au nom du nœud d’élément de données qui contient la valeur Short non signée.

``` syntax
<xs:simpleType name="LengthType">
    <xs:union
        memberValues="unsignedShort string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





