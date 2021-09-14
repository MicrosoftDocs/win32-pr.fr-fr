---
title: MonthlyDOWTrigger. WeeksOfMonth, propriété
description: Pour les scripts, obtient ou définit les semaines du mois pendant lequel la tâche s’exécute.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Planificateur de tâches de la propriété WeeksOfMonth
- Planificateur de tâches de la propriété WeeksOfMonth, objet MonthlyDOWTrigger
- Planificateur de tâches objet MonthlyDOWTrigger, propriété WeeksOfMonth
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013423"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a>MonthlyDOWTrigger. WeeksOfMonth, propriété

Pour les scripts, obtient ou définit les semaines du mois pendant lequel la tâche s’exécute.

## <a name="syntax"></a>Syntaxe


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a>Valeur de la propriété

Un masque de bits qui indique les jours de la semaine pendant lesquels la tâche s’exécute.

## <a name="remarks"></a>Notes

Le tableau suivant montre le mappage du masque de bits utilisé par cette propriété.



| Semaine                     | Valeur hexadécimale | Valeur décimale |
|--------------------------|-----------|---------------|
| Première semaine du mois  | 0X01      | 1             |
| Deuxième semaine du mois | 0x02      | 2             |
| Troisième semaine du mois  | 0X04      | 4             |
| Quatrième semaine du mois | 0X08      | 8             |



 

Lors de la lecture ou de l’écriture de données XML pour une tâche, les jours de la semaine d’un calendrier de jour de semaine mensuel sont spécifiés par l’élément [**weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) .

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

 

 





