---
title: Élément ScheduleByMonth (calendarTriggerType)
description: Spécifie une planification mensuelle.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- Élément ScheduleByMonth Planificateur de tâches
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a03fcc3b30e4fe684926baaba2815132c9f2f06bf4373b4e9fbbc181e187bf6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513809"
---
# <a name="schedulebymonth-calendartriggertype-element"></a>Élément ScheduleByMonth (calendarTriggerType)

Spécifie une planification mensuelle. Par exemple, la tâche commence à 8:00 AM sur des jours spécifiques du mois sur des mois spécifiques.

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

L’élément **ScheduleByMonth** est défini par le type complexe [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                             | Dérivé de                                                                       | Description                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Spécifie un déclencheur quotidien, hebdomadaire, mensuel ou un jour de la semaine (DOW) mensuel.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                  | Type                                                                       | Description                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Spécifie les jours du mois pendant lesquels la tâche est exécutée.<br/>  |
| [**Mois (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)           | [**monthsType**](taskschedulerschema-monthstype-complextype.md)           | Spécifie les mois de l’année pendant laquelle la tâche s’exécute.<br/> |



## <a name="remarks"></a>Remarques

L’heure de début de la tâche est définie par l’élément [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Pour le développement de scripts, un déclencheur mensuel est spécifié à l’aide de l’objet [**MonthlyTrigger**](monthlytrigger.md) .

Pour le développement C++, un déclencheur mensuel est spécifié à l’aide de l’interface [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) .

Les éléments enfants répertoriés ci-dessous sont définis par les types d’éléments complexes [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un déclencheur de calendrier mensuel qui démarre une tâche (à 8:00 AM) le 1er et le quinzième jour de chaque mois de l’année.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
    </ScheduleByMonth>
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

 

 





