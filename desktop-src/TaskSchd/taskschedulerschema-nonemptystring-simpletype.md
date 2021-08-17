---
title: Type simple nonEmptyStringType
description: Définit les valeurs utilisées pour une chaîne de texte non vide.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- Planificateur de tâches de type simple nonEmptyString
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6359240c2baba14460ab4478c31c490725646130ea2181efdcb8e92a94090d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758415"
---
# <a name="nonemptystringtype-simple-type"></a>Type simple nonEmptyStringType

Définit les valeurs utilisées pour une chaîne de texte non vide.

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **nonEmptyString** définit la valeur suivante.



| Valeur | Description                                            |
|-------|--------------------------------------------------------|
| 1     | La chaîne contient au moins un caractère.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





