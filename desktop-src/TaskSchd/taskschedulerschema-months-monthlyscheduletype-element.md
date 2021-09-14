---
title: Élément months (monthlyScheduleType)
description: Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
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
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228654"
---
# <a name="months-monthlyscheduletype-element"></a>Élément months (monthlyScheduleType)

Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

L’élément **months** est défini par le type complexe [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                    | Dérivé de                                                                       | Description                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) | Spécifie une planification mensuelle. <br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                            | Type | Description                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Avril (monthsType)**](taskschedulerschema-april-monthstype-element.md)         |      | Spécifie que la tâche s’exécute en avril.<br/>     |
| [**Août (monthsType)**](taskschedulerschema-august-monthstype-element.md)       |      | Spécifie que la tâche s’exécute en août.<br/>    |
| [**Décembre (monthsType)**](taskschedulerschema-december-monthstype-element.md)   |      | Spécifie que la tâche s’exécute en décembre.<br/>  |
| [**Février (monthsType)**](taskschedulerschema-february-monthstype-element.md)   |      | Spécifie que la tâche s’exécute en février.<br/>  |
| [**Janvier (monthsType)**](taskschedulerschema-january-monthstype-element.md)     |      | Spécifie que la tâche s’exécute en janvier.<br/>   |
| [**Juillet (monthsType)**](taskschedulerschema-july-monthstype-element.md)           |      | Spécifie que la tâche s’exécute en juillet.<br/>      |
| [**Juin (monthsType)**](taskschedulerschema-june-monthstype-element.md)           |      | Spécifie que la tâche s’exécute en juin.<br/>      |
| [**Mars (monthsType)**](taskschedulerschema-march-monthstype-element.md)         |      | Spécifie que la tâche s’exécute en mars.<br/>     |
| [**Mai (monthsType)**](taskschedulerschema-may-monthstype-element.md)             |      | Spécifie que la tâche s’exécute en mai.<br/>       |
| [**Novembre (monthsType)**](taskschedulerschema-november-monthstype-element.md)   |      | Spécifie que la tâche s’exécute en novembre.<br/>  |
| [**Octobre (monthsType)**](taskschedulerschema-october-monthstype-element.md)     |      | Spécifie que la tâche s’exécute en octobre.<br/>   |
| [**Septembre (monthsType)**](taskschedulerschema-september-monthstype-element.md) |      | Spécifie que la tâche s’exécute en septembre.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, les mois de la planification sont spécifiés à l’aide de la propriété [**MonthlyTrigger. MonthsOfYear**](monthlytrigger-monthsofyear.md) .

Pour le développement C++, les mois de la planification sont spécifiés à l’aide de la propriété [**IMonthlyTrigger :: MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un calendrier mensuel qui démarre la tâche le 1er et le quinzième jour de chaque mois de l’année.


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
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

 

 





