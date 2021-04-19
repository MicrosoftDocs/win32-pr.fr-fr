---
title: Élément DaysOfMonth (monthlyScheduleType)
description: Spécifie les jours du mois pendant lesquels la tâche est exécutée.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- Élément DaysOfMonth Planificateur de tâches
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513834"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a>Élément DaysOfMonth (monthlyScheduleType)

Spécifie les jours du mois pendant lesquels la tâche est exécutée.

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

L’élément **DaysOfMonth** est défini par le type complexe [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                    | Dérivé de                                                                                         | Description                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Spécifie un déclencheur qui démarre un travail pour une planification mensuelle de jour de semaine.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                        | Type                                                                    | Description                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**Temps**](taskschedulerschema-day-daysofmonthtype-element.md) | [**dayOfMonthType**](taskschedulerschema-dayofmonthtype-simpletype.md) | Spécifie un jour du mois pendant lequel la tâche s’exécute.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, les jours du mois pour la planification sont spécifiés à l’aide de la propriété [**MonthlyTrigger. DaysOfMonth**](monthlytrigger-daysofmonth.md) .

Pour le développement C++, les jours du mois pour la planification sont spécifiés à l’aide de la propriété [**IMonthlyTrigger ::D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) .

L’élément enfant doit être répété pour chaque jour du mois où la tâche doit être exécutée.

## <a name="examples"></a>Exemples

Le code XML suivant définit un déclencheur de calendrier mensuel qui démarre une tâche (à 8:30 AM) le 1er jour de chaque mois.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
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

 

 





