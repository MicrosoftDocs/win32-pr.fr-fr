---
title: DaysOfWeek (weeklyScheduleType) (élément)
description: Spécifie les jours de la semaine d’exécution de la tâche. | DaysOfWeek (weeklyScheduleType) (élément)
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
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
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106532404"
---
# <a name="daysofweek-weeklyscheduletype-element"></a>DaysOfWeek (weeklyScheduleType) (élément)

Spécifie les jours de la semaine d’exécution de la tâche.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

L’élément **DaysOfWeek** est défini par le type complexe [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                  | Dérivé de                                                                     | Description                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | Spécifie une planification hebdomadaire.<br/> |



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

Les éléments enfants précédents sont définis par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

Pour le développement de script, l’intervalle hebdomadaire est spécifié à l’aide de la propriété [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .

Pour le développement C++, l’intervalle hebdomadaire est spécifié à l’aide de la propriété [**IWeeklyTrigger :: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un déclencheur de calendrier quotidien qui démarre une tâche du lundi au vendredi (à 8:00 AM) chaque semaine.


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



Pour obtenir un exemple complet du code XML d’une tâche qui utilise un déclencheur hebdomadaire, consultez [exemple de déclencheur hebdomadaire (XML)](weekly-trigger-example--xml-.md).

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

 

 





