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
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515086"
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



## <a name="remarks"></a>Notes

Lorsque vous spécifiez les semaines du mois, utilisez les nombres 1-4 pour les quatre premières semaines du mois ou utilisez la chaîne « Last » pour indiquer la semaine dernière du mois.

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

 

 





