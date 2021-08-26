---
title: Élément mai (monthsType)
description: Spécifie que la tâche s’exécute en mai.
ms.assetid: 1fcc3eb7-6500-4ba3-b146-14d169d9b445
keywords:
- Élément de mai Planificateur de tâches
topic_type:
- apiref
api_name:
- May
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d8a7edc0429b77042a5ef7bbb6e16bf69bda8a4c6ed889bbf8c1b981b912ab1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905609"
---
# <a name="may-monthstype-element"></a>Élément mai (monthsType)

Spécifie que la tâche s’exécute en mai.

``` syntax
<xs:element name="May">
    <xs:complexType />
</xs:element>
```

L’élément **peut être** défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                          | Dérivé de                                                     | Description                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Mois (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.<br/> |
| [**Mois (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.<br/>             |



## <a name="examples"></a>Exemples

Le code XML suivant définit un calendrier de mois qui exécute la tâche dans mai.


```XML
<Months>
    <May/>
</Months>
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

 

 





