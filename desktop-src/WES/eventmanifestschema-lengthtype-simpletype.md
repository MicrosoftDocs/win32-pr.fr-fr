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
ms.openlocfilehash: dbb0720c2e26fa73056ccffdd17392e93e491c11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191819"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





