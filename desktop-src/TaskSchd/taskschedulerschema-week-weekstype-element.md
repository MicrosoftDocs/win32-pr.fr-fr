---
title: Élément week (weeksType)
description: Spécifie une semaine spécifique du mois.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Élément week Planificateur de tâches
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a999eaa5ec7d4ed36b86fc292f4c0d5e8c474fd1df8f5f4b9da5b90f2dcca641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758205"
---
# <a name="week-weekstype-element"></a>Élément week (weeksType)

Spécifie une semaine spécifique du mois.

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

L’élément **week** est défini par le type complexe [**weeksType**](taskschedulerschema-weekstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                                        | Dérivé de                                                   | Description                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [**Semaines (monthlyDayOfWeekScheduleType)**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [**weeksType**](taskschedulerschema-weekstype-complextype.md) | Spécifie les semaines du mois où la tâche est exécutée.<br/> |



## <a name="remarks"></a>Remarques

Lorsque vous spécifiez les semaines du mois, utilisez les nombres 1-4 pour les quatre premières semaines du mois ou utilisez la chaîne « Last » pour indiquer la semaine dernière du mois.

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

 

 





