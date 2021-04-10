---
title: Élément ScheduleByDay (calendarTriggerType)
description: Spécifie une planification quotidienne.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- déclencheur quotidien Planificateur de tâches, élément XML
- Élément ScheduleByDay Planificateur de tâches
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942618"
---
# <a name="schedulebyday-calendartriggertype-element"></a>Élément ScheduleByDay (calendarTriggerType)

Spécifie une planification quotidienne. Par exemple, la tâche commence à 8:00 AM tous les jours, tous les jours, tous les trois jours, et ainsi de suite.

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

L’élément **ScheduleByDay** est défini par le type complexe [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                             | Dérivé de                                                                       | Description                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                            | Type             | Description                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | **unsignedByte** | Spécifie l’intervalle entre les jours de la planification.<br/> |



## <a name="remarks"></a>Notes

L’élément enfant listé précédemment est défini par les types d’éléments complexes [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .

L’heure de début de la tâche est définie par l’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Pour le développement de script, un déclencheur quotidien est spécifié à l’aide de l’objet [**DailyTrigger**](weeklytrigger.md) .

Pour le développement C++, un déclencheur quotidien est spécifié à l’aide de l’interface [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un déclencheur de calendrier quotidien qui démarre la tâche tous les jours.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Pour obtenir un exemple complet du code XML d’une tâche qui spécifie une planification quotidienne, consultez [exemple de déclencheur quotidien (XML)](daily-trigger-example--xml-.md).

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

 

 





