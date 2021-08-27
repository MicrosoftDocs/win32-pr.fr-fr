---
title: Type complexe idleTriggerType
description: Définit le type de base pour l’élément IdleTrigger.
ms.assetid: 05beabb7-2e6f-4df1-809a-9f64a578d80a
keywords:
- Planificateur de tâches de type complexe idleTriggerType
topic_type:
- apiref
api_name:
- idleTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5c1ae0c6a88576eb7996a8151e96bb92c4a47c0d732a3558deede3b835356f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100019"
---
# <a name="idletriggertype-complex-type"></a>Type complexe idleTriggerType

Définit le type de base pour l’élément [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="idleTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
         />
    </xs:complexContent>
</xs:complexType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





