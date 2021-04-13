---
title: MonthlyDOWTrigger. DaysOfWeek, propriété
description: Pour les scripts, obtient ou définit les jours de la semaine pendant lesquels la tâche est exécutée.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- DaysOfWeek, propriété Planificateur de tâches
- DaysOfWeek, propriété Planificateur de tâches, objet MonthlyDOWTrigger
- Objet MonthlyDOWTrigger Planificateur de tâches, DaysOfWeek, propriété
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466442"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>MonthlyDOWTrigger. DaysOfWeek, propriété

Pour les scripts, obtient ou définit les jours de la semaine pendant lesquels la tâche est exécutée.

## <a name="syntax"></a>Syntaxe


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valeur de la propriété

Un masque de bits qui indique les jours de la semaine pendant lesquels la tâche s’exécute.

## <a name="remarks"></a>Notes

Le tableau suivant montre le mappage du masque de bits utilisé par cette propriété.



| Jour de la semaine | Valeur hexadécimale | Valeur décimale |
|-------------|-----------|---------------|
| Dimanche      | 0x01      | 1             |
| Lundi      | 0x02      | 2             |
| Mardi     | 0x04      | 4             |
| Mercredi   | 0x08      | 8             |
| Thursday    | 0x10      | 16            |
| Vendredi      | 0x20      | 32            |
| Samedi    | 0x40      | 64            |



 

Lors de la lecture ou de l’écriture de données XML pour une tâche, les jours de la semaine d’un calendrier de jour de semaine mensuel sont spécifiés par l’élément [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





