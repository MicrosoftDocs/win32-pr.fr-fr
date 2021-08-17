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
ms.openlocfilehash: c7ed2a597c1b92245a34dae510c079a5b5aa7a4e7893a78dbb70d7bc5988d580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357139"
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
| [**Lundi**](taskschedulerschema-monday-daysofweektype-element.md)       |      | Spécifie que la tâche est exécutée le lundi.<br/>    |
| [**Samedi**](taskschedulerschema-saturday-daysofweektype-element.md)   |      | Spécifie que la tâche est exécutée le samedi.<br/>  |
| [**Dimanche**](taskschedulerschema-sunday-daysofweektype-element.md)       |      | Spécifie que la tâche est exécutée le dimanche.<br/>    |
| [**Thursday**](taskschedulerschema-thursday-daysofweektype-element.md)   |      | Spécifie que la tâche est exécutée le jeudi.<br/>  |
| [**Mardi**](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | Spécifie que la tâche est exécutée le mardi.<br/>   |
| [**Mercredi**](taskschedulerschema-wednesday-daysofweektype-element.md) |      | Spécifie que la tâche est exécutée le mercredi.<br/> |



## <a name="remarks"></a>Remarques

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





