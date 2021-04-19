---
title: Type complexe monthlyDayOfWeekScheduleType
description: Définit les éléments enfants et les informations de séquencement pour l’élément ScheduleByMonthDayOfWeek.
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- Planificateur de tâches de type complexe monthlyDayOfWeekScheduleType
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 782715aed5cbf59a98e996bfa18fdd7c1022227a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543057"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a>Type complexe monthlyDayOfWeekScheduleType

Définit les éléments enfants et les informations de séquencement pour l’élément [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) .

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                   | Type                                                                     | Description                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Spécifie les jours de la semaine pendant lesquels la tâche est exécutée.<br/>   |
| [**Suivent**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthsType**](taskschedulerschema-monthstype-complextype.md)         | Spécifie les mois de l’année pendant laquelle la tâche s’exécute.<br/> |
| [**Semaines**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [**weeksType**](taskschedulerschema-weekstype-complextype.md)           | Spécifie les semaines du mois pendant lequel la tâche s’exécute.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





