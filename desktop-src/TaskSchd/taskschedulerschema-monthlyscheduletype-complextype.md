---
title: Type complexe monthlyScheduleType
description: Définit les éléments enfants et les informations de séquencement pour l’élément ScheduleByMonth (calendarTriggerType).
ms.assetid: 3ade775c-ca44-403e-9602-80095c7dba1a
keywords:
- Planificateur de tâches de type complexe monthlyScheduleType
topic_type:
- apiref
api_name:
- monthlyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06bb8786e817c59209d4b3807d119c017a6a04ae3eff5cfe623b76d57e04b9f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991139"
---
# <a name="monthlyscheduletype-complex-type"></a>Type complexe monthlyScheduleType

Définit les éléments enfants et les informations de séquencement pour l’élément [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) .

``` syntax
<xs:complexType name="monthlyScheduleType">
    <xs:all>
        <xs:element name="DaysOfMonth"
            type="daysOfMonthType"
            minOccurs="0"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                            | Type                                                                       | Description                                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Spécifie les jours du mois pendant lesquels la tâche est exécutée.<br/>                         |
| [**Suivent**](taskschedulerschema-months-monthlyscheduletype-element.md)           | [**monthsType**](taskschedulerschema-monthstype-complextype.md)           | Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.<br/> |



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

 

 





