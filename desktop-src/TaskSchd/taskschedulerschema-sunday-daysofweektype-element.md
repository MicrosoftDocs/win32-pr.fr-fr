---
title: Sunday (daysOfWeekType) (élément)
description: Spécifie que la tâche est exécutée le dimanche.
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- Sunday, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40efba31b392da5959853feeb1cae567cee25cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105352"
---
# <a name="sunday-daysofweektype-element"></a>Sunday (daysOfWeekType) (élément)

Spécifie que la tâche est exécutée le dimanche.

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

L’élément **Sunday** est défini par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                                  | Dérivé de                                                             | Description                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification mensuelle de jour de semaine.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification hebdomadaire.<br/>              |



## <a name="examples"></a>Exemples

Le code XML suivant définit un calendrier de jour de semaine qui démarre une tâche le dimanche.


```XML
<DaysOfWeek>
    <Sunday/>
</DaysOfWeek>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





