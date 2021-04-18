---
title: WeeklyTrigger. DaysOfWeek, propriété
description: Pour les scripts, obtient ou définit les jours de la semaine où la tâche est exécutée.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- DaysOfWeek, propriété Planificateur de tâches
- DaysOfWeek, propriété Planificateur de tâches, objet WeeklyTrigger
- Objet WeeklyTrigger Planificateur de tâches, DaysOfWeek, propriété
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519257"
---
# <a name="weeklytriggerdaysofweek-property"></a>WeeklyTrigger. DaysOfWeek, propriété

Pour les scripts, obtient ou définit les jours de la semaine où la tâche est exécutée.

## <a name="syntax"></a>Syntaxe


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valeur de la propriété

Un masque de bits qui indique les jours de la semaine où la tâche est exécutée.

## <a name="remarks"></a>Notes

Le tableau suivant montre le mappage du masque de bits utilisé par cette propriété.



| Month     | Valeur hexadécimale | Valeur décimale |
|-----------|-----------|---------------|
| Dimanche    | 0X01      | 1             |
| Lundi    | 0x02      | 2             |
| Mardi   | 0X04      | 4             |
| Mercredi | 0X08      | 8             |
| Thursday  | 0X10      | 16            |
| Vendredi    | 0x20      | 32            |
| Samedi  | 0X40      | 64            |



 

Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, les jours de la semaine sont spécifiés à l’aide de l’élément [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





