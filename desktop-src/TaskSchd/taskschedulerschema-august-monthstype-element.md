---
title: Élément d’août (monthsType)
description: Spécifie que la tâche s’exécute en août.
ms.assetid: cd7e528c-d482-4bb4-a31f-fccdb19a441b
keywords:
- Planificateur de tâches de l’élément d’août
topic_type:
- apiref
api_name:
- August
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4978ebd8f22da6e157461791c4c2000fce9db6ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843857"
---
# <a name="august-monthstype-element"></a>Élément d’août (monthsType)

Spécifie que la tâche s’exécute en août.

``` syntax
<xs:element name="August">
    <xs:complexType />
</xs:element>
```

L’élément d' **août** est défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                          | Dérivé de                                                     | Description                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Mois (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.<br/> |
| [**Mois (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.<br/>             |



## <a name="examples"></a>Exemples

Le code XML suivant définit un calendrier de mois qui exécute la tâche en août.


```XML
<Months>
    <August/>
</Months>
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

 

 





