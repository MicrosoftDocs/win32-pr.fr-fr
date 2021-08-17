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
ms.openlocfilehash: 81219236012146dac54965af471412369d5c5bb34319897d4d821bb10a730aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757976"
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



## <a name="remarks"></a>Remarques

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





