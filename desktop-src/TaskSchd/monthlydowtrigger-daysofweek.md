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
ms.openlocfilehash: 0b9abf5dcd33c92d402f8ed6047a2fd80a0d5905bae075110931cfb8f83aa10a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517459"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>MonthlyDOWTrigger. DaysOfWeek, propriété

Pour les scripts, obtient ou définit les jours de la semaine pendant lesquels la tâche est exécutée.

## <a name="syntax"></a>Syntaxe


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valeur de la propriété

Un masque de bits qui indique les jours de la semaine pendant lesquels la tâche s’exécute.

## <a name="remarks"></a>Remarques

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





