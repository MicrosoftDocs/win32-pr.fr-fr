---
title: Élément de novembre (monthsType)
description: Spécifie que la tâche s’exécute en novembre.
ms.assetid: 45f8c47b-3884-4f18-8275-f29f82ee32e2
keywords:
- Planificateur de tâches de l’élément de novembre
topic_type:
- apiref
api_name:
- November
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 295b63a4ff4dad1ec07504bb43c4a471d4389159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536293"
---
# <a name="november-monthstype-element"></a>Élément de novembre (monthsType)

Spécifie que la tâche s’exécute en novembre.

``` syntax
<xs:element name="November">
    <xs:complexType />
</xs:element>
```

L’élément **novembre** est défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                          | Dérivé de                                                     | Description                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Mois (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.<br/> |
| [**Mois (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.<br/>             |



## <a name="examples"></a>Exemples

Le code XML suivant définit un calendrier de mois qui exécute la tâche en novembre.


```XML
<Months>
    <November/>
</DaysOfWeek>
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

 

 





