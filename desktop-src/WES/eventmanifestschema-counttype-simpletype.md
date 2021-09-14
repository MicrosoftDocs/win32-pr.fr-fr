---
title: Type simple CountType
description: Définit un type de nombre qui est utilisé pour spécifier le nombre d’éléments dans un tableau.
ms.assetid: 84f819d7-5c42-475b-9144-aaa5e2d215c8
keywords:
- Journal des types simples CountType
topic_type:
- apiref
api_name:
- CountType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f91b19df4182f5cff305de0429a308d0c5db234
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919572"
---
# <a name="counttype-simple-type"></a>Type simple CountType

Définit un type de nombre qui est utilisé pour spécifier le nombre d’éléments dans un tableau. La valeur peut être spécifiée sous la forme d’une valeur XS : unsignedShort ou sous la forme d’une chaîne qui fait référence au nom du nœud d’élément de données qui contient la valeur Short unsiged.

``` syntax
<xs:simpleType name="CountType">
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



 

 





