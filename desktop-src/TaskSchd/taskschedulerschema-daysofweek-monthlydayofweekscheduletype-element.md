---
title: DaysOfWeek (monthlyDayOfWeekScheduleType) (élément)
description: Spécifie les jours de la semaine d’exécution de la tâche. | DaysOfWeek (monthlyDayOfWeekScheduleType) (élément)
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
keywords:
- DaysOfWeek, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523156"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a>DaysOfWeek (monthlyDayOfWeekScheduleType) (élément)

Spécifie les jours de la semaine d’exécution de la tâche.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

L’élément **DaysOfWeek** est défini par le type complexe [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                      | Dérivé de                                                                                         | Description                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Spécifie un déclencheur qui démarre un travail pour une planification mensuelle de jour de semaine.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                   | Type | Description                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Vendredi**](taskschedulerschema-friday-daysofweektype-element.md)       |      | Spécifie que la tâche est exécutée le vendredi.<br/>    |
| [**Monday**](taskschedulerschema-monday-daysofweektype-element.md)       |      | Spécifie que la tâche est exécutée le lundi.<br/>    |
| [**Samedi**](taskschedulerschema-saturday-daysofweektype-element.md)   |      | Spécifie que la tâche est exécutée le samedi.<br/>  |
| [**Dimanche**](taskschedulerschema-sunday-daysofweektype-element.md)       |      | Spécifie que la tâche est exécutée le dimanche.<br/>    |
| [**Thursday**](taskschedulerschema-thursday-daysofweektype-element.md)   |      | Spécifie que la tâche est exécutée le jeudi.<br/>  |
| [**Mardi**](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | Spécifie que la tâche est exécutée le mardi.<br/>   |
| [**Mercredi**](taskschedulerschema-wednesday-daysofweektype-element.md) |      | Spécifie que la tâche est exécutée le mercredi.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, les jours de la semaine pour un calendrier mensuel de jour de la semaine sont spécifiés à l’aide de la propriété [**MonthlyDOWTrigger. DaysOfWeek**](monthlydowtrigger-daysofweek.md) .

Pour le développement C++, les jours de la semaine pour un calendrier mensuel de jour de semaine sont spécifiés à l’aide de la propriété [**IMonthlyDOWTrigger ::D aysofweek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) .

Les éléments enfants ci-dessus sont définis par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un calendrier mensuel de jour de semaine qui démarre la tâche le lundi de la première semaine pour chaque mois de l’année.


```XML
<ScheduleByMonthDayOfWeek>
    <Weeks>
        <Week>1</Week>
    </Weeks>
    <DaysOfWeek>
        <Monday/>
    </DaysOfWeek>
    <Months>
        <January/>
        <February/>
        <March/>
        <April/>
        <May/>
        <June/>
        <July/>
        <August/>
        <September/>
        <October/>
        <November/>
        <December/>
    <Months>
</ScheduleByMonthDayOfWeek>
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

 

 





