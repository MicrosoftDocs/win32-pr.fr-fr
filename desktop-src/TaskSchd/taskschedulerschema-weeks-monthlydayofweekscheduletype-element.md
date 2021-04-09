---
title: Semaines (élément monthlyDayOfWeekScheduleType)
description: Spécifie les semaines du mois où la tâche est exécutée.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Planificateur de tâches de l’élément weeks
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743309"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a>Semaines (élément monthlyDayOfWeekScheduleType)

Spécifie les semaines du mois où la tâche est exécutée.

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

L’élément **weeks** est défini par le type complexe [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                      | Dérivé de                                                                                         | Description                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Spécifie un déclencheur qui démarre un travail sur une planification de jour de semaine mensuelle.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                    | Type                                                        | Description                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [**Week**](taskschedulerschema-week-weekstype-element.md) | [**weekType**](taskschedulerschema-weektype-simpletype.md) | Spécifie une semaine spécifique du mois.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, les semaines du mois sont spécifiées à l’aide de la propriété [**MonthlyDOWTrigger. WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) .

Pour le développement C++, les semaines du mois sont spécifiées à l’aide de la propriété [**IMonthlyDOWTrigger :: WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) .

Lorsque vous spécifiez les semaines du mois, utilisez 1-4 pour spécifier les quatre premières semaines du mois ou utilisez la chaîne « Last » pour indiquer la dernière semaine, quelle que soit la semaine.

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

 

 





