---
title: Élément de février (monthsType)
description: Spécifie que la tâche s’exécute en février.
ms.assetid: 871449f8-fa3a-4e1f-be36-bc5c98125721
keywords:
- Planificateur de tâches de l’élément de février
topic_type:
- apiref
api_name:
- February
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727751964bfb9a752eb1190f8c7d3a86de2a9413
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228852"
---
# <a name="february-monthstype-element"></a>Élément de février (monthsType)

Spécifie que la tâche s’exécute en février.

``` syntax
<xs:element name="February">
    <xs:complexType />
</xs:element>
```

L’élément de **février** est défini par le type complexe [**monthsType**](taskschedulerschema-monthstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                          | Dérivé de                                                     | Description                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Mois (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle de jour de semaine.<br/> |
| [**Mois (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Spécifie les mois de l’année pendant laquelle la tâche s’exécute pour une planification mensuelle.<br/>             |



## <a name="examples"></a>Exemples

Le code XML suivant définit un calendrier de mois qui exécute la tâche en février.


```XML
<Months>
    <February/>
</Months>
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

 

 





