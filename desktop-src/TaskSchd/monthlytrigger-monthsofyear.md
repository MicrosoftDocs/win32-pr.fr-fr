---
title: MonthlyTrigger. MonthsOfYear, propriété
description: Pour les scripts, obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute. | MonthlyTrigger. MonthsOfYear, propriété
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- Planificateur de tâches de la propriété MonthsOfYear
- Planificateur de tâches de la propriété MonthsOfYear, objet MonthlyTrigger
- Planificateur de tâches objet MonthlyTrigger, propriété MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff6f08e257acf85a8a3f073f43c3c81e65817900f8154e1701ab73fe10c2368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253779"
---
# <a name="monthlytriggermonthsofyear-property"></a>MonthlyTrigger. MonthsOfYear, propriété

Pour les scripts, obtient ou définit les mois de l’année pendant laquelle la tâche s’exécute.

## <a name="syntax"></a>Syntaxe


```VB
MonthlyTrigger.MonthsOfYear As short
```



## <a name="property-value"></a>Valeur de la propriété

Un masque de bits qui indique les mois de l’année pendant laquelle la tâche s’exécute.

## <a name="remarks"></a>Remarques

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



 

Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, les mois de l’année sont spécifiés à l’aide de l’élément [**months**](taskschedulerschema-months-monthlyscheduletype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**MonthlyTrigger**](monthlytrigger.md)
</dt> </dl>

 

 





