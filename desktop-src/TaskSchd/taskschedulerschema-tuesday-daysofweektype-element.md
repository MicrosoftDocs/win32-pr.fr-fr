---
title: Tuesday (daysOfWeekType) (élément)
description: Spécifie que la tâche est exécutée le mardi.
ms.assetid: 588608e9-33f9-405d-8b4b-35f11ab403db
keywords:
- Tuesday, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Tuesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524d5dbe6b0deb1636fd06281d81b641665609310ad10a8b407da2dc570876ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355612"
---
# <a name="tuesday-daysofweektype-element"></a>Tuesday (daysOfWeekType) (élément)

Spécifie que la tâche est exécutée le mardi.

``` syntax
<xs:element name="Tuesday">
    <xs:complexType />
</xs:element>
```

L’élément **Tuesday** est défini par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                                  | Dérivé de                                                             | Description                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification mensuelle de jour de semaine.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification hebdomadaire.<br/>              |



## <a name="examples"></a>Exemples

Le code XML suivant définit un calendrier de jour de semaine qui démarre une tâche le mardi.


```XML
<DaysOfWeek>
    <Tuesday/>
</DaysOfWeek>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





