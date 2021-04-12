---
title: Élément ScheduleByWeek (calendarTriggerType)
description: Spécifie une planification hebdomadaire.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- déclencheur hebdomadaire Planificateur de tâches, élément XML
- Élément ScheduleByWeek Planificateur de tâches
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385183"
---
# <a name="schedulebyweek-calendartriggertype-element"></a>Élément ScheduleByWeek (calendarTriggerType)

Spécifie une planification hebdomadaire. Par exemple, la tâche commence à 8:00 AM un jour spécifique de la semaine chaque semaine ou un jour spécifique de la semaine chaque semaine.

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

L’élément **ScheduleByWeek** est défini par le type complexe [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                             | Dérivé de                                                                       | Description                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                               | Type                                                                     | Description                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Spécifie les jours de la semaine d’exécution de la tâche.<br/>    |
| [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | unsignedByte                                                             | Spécifie l’intervalle entre les semaines de la planification.<br/> |



## <a name="remarks"></a>Notes

Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .

L’heure de début de la tâche est définie par l’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Pour le développement de script, un déclencheur hebdomadaire est spécifié à l’aide de l’objet [**WeeklyTrigger**](weeklytrigger.md) .

Pour le développement C++, un déclencheur hebdomadaire est spécifié à l’aide de l’interface [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un déclencheur de calendrier hebdomadaire qui démarre une tâche du lundi au vendredi (à 8:00 AM) chaque semaine.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
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

 

 





