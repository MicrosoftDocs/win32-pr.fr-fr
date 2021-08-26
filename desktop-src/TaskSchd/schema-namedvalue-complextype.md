---
title: Type complexe namedValue
description: Définit un nom qui est associé à une valeur dans une paire nom-valeur.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- Planificateur de tâches de type complexe namedValue
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f0f92b89114dfedfbfdbc61d476aff99332191317c1f67b2163eb9416ef3a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080419"
---
# <a name="namedvalue-complex-type"></a>Type complexe namedValue

Définit un nom qui est associé à une valeur dans une paire nom-valeur.

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributs



| Nom | Type                                                                    | Description                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| name | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Spécifie le nom qui est associé à une valeur dans une paire nom-valeur. <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





