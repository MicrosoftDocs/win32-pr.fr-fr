---
title: Type complexe calendarTriggerType
description: Définit les éléments enfants et les informations de séquencement pour les éléments de calendrier.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- Planificateur de tâches de type complexe calendarTriggerType
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 62b6aa2c3c1aff0e6e9cb706ede58c1b21af79fb7a5bae812a992e68bbd28b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866649"
---
# <a name="calendartriggertype-complex-type"></a>Type complexe calendarTriggerType

Définit les éléments enfants et les informations de séquencement pour les éléments de calendrier.

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                      | Type                                                                                                 | Description                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RandomDelay**](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | duration                                                                                             | Contient le délai d’attente ajouté de manière aléatoire à l’heure de début du déclencheur. Le format de cette chaîne est `P<days>DT<hours>H<minutes>M<seconds>S` (par exemple, P2DT5S est un délai de 2 jours, 5 secondes).<br/> |
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Spécifie une planification quotidienne. Par exemple, la tâche démarre tous les jours, tous les jours, tous les trois jours, et ainsi de suite.<br/>                                                                                                               |
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Spécifie une planification mensuelle. Par exemple, la tâche commence à 8:00 AM sur des jours spécifiques du mois sur des mois spécifiques. <br/>                                                                                                       |
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Spécifie un déclencheur qui démarre un travail sur une planification de jour de semaine mensuelle. Par exemple, la tâche démarre des jours spécifiques de la semaine, des semaines du mois et des mois de l’année. <br/>                                               |
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Spécifie une planification hebdomadaire. Par exemple, la tâche commence à 8:00 AM un jour spécifique de la semaine chaque semaine ou un jour spécifique de la semaine chaque semaine. <br/>                                                              |



## <a name="remarks"></a>Remarques

En plus de l’élément enfant défini ici, l’élément [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) utilise également les éléments enfants définis par le type complexe [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





