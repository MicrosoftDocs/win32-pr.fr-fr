---
title: Type complexe triggersType
description: Définit le groupe (triggerGroup) pour tous les éléments déclencheurs.
ms.assetid: ceabc332-e028-491e-8fd8-c02ac23a2635
keywords:
- Planificateur de tâches de type complexe triggersType
topic_type:
- apiref
api_name:
- triggersType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c2bd6fa4011841958ad08239640024f9878528aecb1307487c3354ac74e31db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610536"
---
# <a name="triggerstype-complex-type"></a>Type complexe triggersType

Définit le groupe ([**triggerGroup**](taskschedulerschema-triggergroup-group.md)) pour tous les éléments déclencheurs. Le groupe [**triggerGroup**](taskschedulerschema-triggergroup-group.md) contient la liste des déclencheurs qui peuvent être utilisés dans une tâche.

``` syntax
<xs:complexType name="triggersType">
    <xs:group
        minOccurs="0"
        maxOccurs="48"
        ref="triggerGroup"
     />
</xs:complexType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





