---
title: MonthlyDOWTrigger. MonthsOfYear, propriété
description: Pour les scripts, obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute. | MonthlyDOWTrigger. MonthsOfYear, propriété
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- Planificateur de tâches de la propriété MonthsOfYear
- Planificateur de tâches de la propriété MonthsOfYear, objet MonthlyDOWTrigger
- Planificateur de tâches objet MonthlyDOWTrigger, propriété MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869978"
---
# <a name="monthlydowtriggermonthsofyear-property"></a>MonthlyDOWTrigger. MonthsOfYear, propriété

Pour les scripts, obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute.

## <a name="syntax"></a>Syntaxe


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a>Valeur de la propriété

Un masque de bits qui indique les mois de l’année pendant laquelle la tâche s’exécute.

## <a name="remarks"></a>Notes

Le tableau suivant montre le mappage du masque de bits utilisé par cette propriété.



| Month     | Valeur hexadécimale | Valeur décimale |
|-----------|-----------|---------------|
| Janvier   | 0X01      | 1             |
| February  | 0x02      | 2             |
| Mars     | 0X04      | 4             |
| avril     | 0X08      | 8             |
| Mai       | 0X10      | 16            |
| June      | 0X20      | 32            |
| Juillet      | 0x40      | 64            |
| Août    | 0X80      | 128           |
| Septembre | 0X100     | 256           |
| Octobre   | 0X200     | 512           |
| Novembre  | 0X400     | 1 024          |
| Décembre  | 0X800     | 2 048          |



 

Lors de la lecture ou de l’écriture de données XML pour une tâche, les mois de l’année d’un calendrier de jour de semaine mensuel sont spécifiés par l’élément [**months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) du schéma planificateur de tâches.

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

 

 





