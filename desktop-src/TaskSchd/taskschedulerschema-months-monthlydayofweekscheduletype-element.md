---
title: Élément months (monthlyDayOfWeekScheduleType)
description: Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Mois, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228660"
---
# <a name="months-monthlydayofweekscheduletype-element"></a>Élément months (monthlyDayOfWeekScheduleType)

Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

L’élément **months** est défini par le type complexe [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                                            | Dérivé de                                                                                         | Description                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Spécifie un déclencheur qui démarre un travail pour une planification mensuelle de jour de semaine.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                               | Type | Description                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [**avril**](taskschedulerschema-april-monthstype-element.md)         |      | Spécifie que la tâche s’exécute en avril.<br/>     |
| [**Août**](taskschedulerschema-august-monthstype-element.md)       |      | Spécifie que la tâche s’exécute en août.<br/>    |
| [**Décembre**](taskschedulerschema-december-monthstype-element.md)   |      | Spécifie que la tâche s’exécute en décembre.<br/>  |
| [**February**](taskschedulerschema-february-monthstype-element.md)   |      | Spécifie que la tâche s’exécute en février.<br/>  |
| [**Janvier**](taskschedulerschema-january-monthstype-element.md)     |      | Spécifie que la tâche s’exécute en janvier.<br/>   |
| [**Juillet**](taskschedulerschema-july-monthstype-element.md)           |      | Spécifie que la tâche s’exécute en juillet.<br/>      |
| [**June**](taskschedulerschema-june-monthstype-element.md)           |      | Spécifie que la tâche s’exécute en juin.<br/>      |
| [**Mars**](taskschedulerschema-march-monthstype-element.md)         |      | Spécifie que la tâche s’exécute en mars.<br/>     |
| [**Mai**](taskschedulerschema-may-monthstype-element.md)             |      | Spécifie que la tâche s’exécute en mai.<br/>       |
| [**Novembre**](taskschedulerschema-november-monthstype-element.md)   |      | Spécifie que la tâche s’exécute en novembre.<br/>  |
| [**Octobre**](taskschedulerschema-october-monthstype-element.md)     |      | Spécifie que la tâche s’exécute en octobre.<br/>   |
| [**Septembre**](taskschedulerschema-september-monthstype-element.md) |      | Spécifie que la tâche s’exécute en septembre.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, les mois d’une année pour une planification de jour de semaine mensuelle sont spécifiés à l’aide de la propriété [**MonthlyDOWTrigger. MonthsOfYear**](monthlydowtrigger-monthsofyear.md) .

Pour le développement C++, les mois d’une année pour une planification de jour de semaine mensuelle sont spécifiés à l’aide de la propriété [**IMonthlyDOWTrigger :: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) .

Les éléments enfants ci-dessus sont définis par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .

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



## <a name="requirements"></a>Spécifications



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

 

 





