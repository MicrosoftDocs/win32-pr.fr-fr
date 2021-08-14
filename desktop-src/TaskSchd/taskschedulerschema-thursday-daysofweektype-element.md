---
title: Jeudi (daysOfWeekType) (élément)
description: Spécifie que la tâche est exécutée le jeudi.
ms.assetid: 01d0e7e8-7135-4f43-9d8f-b50c002b93bc
keywords:
- Jeudi, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Thursday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 30b042200cfb00545d31196f1d7480c4aec62cc92a1c08eba3a3fd72117d6f13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356067"
---
# <a name="thursday-daysofweektype-element"></a>Jeudi (daysOfWeekType) (élément)

Spécifie que la tâche est exécutée le jeudi.

``` syntax
<xs:element name="Thursday">
    <xs:complexType />
</xs:element>
```

L’élément **Thursday** est défini par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                                  | Dérivé de                                                             | Description                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification mensuelle de jour de semaine.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification hebdomadaire.<br/>              |



## <a name="examples"></a>Exemples

Le code XML suivant définit un calendrier de jour de semaine qui démarre une tâche le jeudi.


```XML
<DaysOfWeek>
    <Thursday/>
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

 

 





