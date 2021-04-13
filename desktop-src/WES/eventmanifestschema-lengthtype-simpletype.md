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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317458"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





