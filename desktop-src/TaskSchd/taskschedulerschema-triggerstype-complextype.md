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
ms.openlocfilehash: 9903fdc292fe832cc6931d794a4c1f39fd91f83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517330"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





