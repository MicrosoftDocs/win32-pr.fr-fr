---
title: Élément ScheduleByMonthDayOfWeek (calendarTriggerType)
description: Spécifie une planification mensuelle du jour de la semaine.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Élément ScheduleByMonthDayOfWeek Planificateur de tâches
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 185608ea5a8805511de8430c82e6eecabd9cc5b9622fed85d71e26dd39f20cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099879"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a>Élément ScheduleByMonthDayOfWeek (calendarTriggerType)

Spécifie une planification mensuelle du jour de la semaine. Par exemple, la tâche démarre des jours spécifiques de la semaine, des semaines du mois et des mois de l’année.

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

L’élément **ScheduleByMonthDayOfWeek** est défini par le type complexe [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                             | Dérivé de                                                                       | Description                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                   | Type                                                                     | Description                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Spécifie les jours de la semaine d’exécution de la tâche.<br/>       |
| [**Suivent**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthsType**](taskschedulerschema-monthstype-complextype.md)         | Spécifie les mois de l’année pendant laquelle la tâche s’exécute.<br/> |
| [**Semaines**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | unsignedByte                                                             | Spécifie l’intervalle entre les semaines de la planification.<br/>    |



## <a name="remarks"></a>Remarques

L’heure de début de la tâche est définie par l’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Pour le développement de scripts, un déclencheur de jour de semaine mensuel est spécifié à l’aide de l’objet [**MonthlyDOWTrigger**](monthlydowtrigger.md) .

Pour le développement C++, un déclencheur de jour de semaine mensuel est spécifié à l’aide de l’interface [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) .

Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un déclencheur de calendrier de jour de semaine mensuel qui démarre une tâche (à 8:00 AM) le lundi de la première semaine pour chaque mois de l’année.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
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

 

 





