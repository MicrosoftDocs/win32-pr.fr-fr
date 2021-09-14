---
title: Samedi (daysOfWeekType) (élément)
description: Spécifie que la tâche est exécutée le samedi.
ms.assetid: def26a72-c143-466a-b5b0-6105078afffa
keywords:
- Samedi, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Saturday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b5f7cb36002b2add64cdea541caa2fd28df37ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233052"
---
# <a name="saturday-daysofweektype-element"></a>Samedi (daysOfWeekType) (élément)

Spécifie que la tâche est exécutée le samedi.

``` syntax
<xs:element name="Saturday">
    <xs:complexType />
</xs:element>
```

L’élément **Saturday** est défini par le type complexe [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                                  | Dérivé de                                                             | Description                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification mensuelle de jour de semaine.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Spécifie les jours de la semaine pendant lesquels la tâche s’exécute pour une planification hebdomadaire.<br/>              |



## <a name="examples"></a>Exemples

Le code XML suivant définit un calendrier de jour de semaine qui démarre une tâche le samedi.


```XML
<DaysOfWeek>
    <Saturday/>
</DaysOfWeek>
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

 

 





