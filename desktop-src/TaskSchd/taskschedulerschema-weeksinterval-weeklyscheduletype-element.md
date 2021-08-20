---
title: Élément WeeksInterval (weeklyScheduleType)
description: Spécifie l’intervalle entre les semaines de la planification.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- Élément WeeksInterval Planificateur de tâches
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c59e4f4b163e5e96418c84bf2925e45cf3a54da1bbb50e17ad9282409438ff3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059757"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a>Élément WeeksInterval (weeklyScheduleType)

Spécifie l’intervalle entre les semaines de la planification.

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément est défini par le type complexe [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                  | Dérivé de                                                                     | Description                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | Spécifie une planification hebdomadaire.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement de script, l’intervalle hebdomadaire est spécifié à l’aide de la propriété [**WeeklyTrigger. WeeksInterval**](weeklytrigger-weeksinterval.md) .

Pour le développement C++, l’intervalle hebdomadaire est spécifié à l’aide de la propriété [**IWeeklyTrigger :: WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





