---
title: MonthlyDOWTrigger. RandomDelay, propriété
description: Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur. | MonthlyDOWTrigger. RandomDelay, propriété
ms.assetid: e5cb6c1d-8003-43f4-bf35-da490a6097f0
keywords:
- Planificateur de tâches de la propriété RandomDelay
- Planificateur de tâches de la propriété RandomDelay, objet MonthlyDOWTrigger
- Planificateur de tâches objet MonthlyDOWTrigger, propriété RandomDelay
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40fd85ca528476d37861a93230e5074ba87f6a3258a140c2616aa98625d4b96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253828"
---
# <a name="monthlydowtriggerrandomdelay-property"></a>MonthlyDOWTrigger. RandomDelay, propriété

Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.

## <a name="syntax"></a>Syntaxe


```VB
MonthlyDOWTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valeur de la propriété

Délai d’ajout aléatoire à l’heure de début du déclencheur. Le format de cette chaîne est `P<days>DT<hours>H<minutes>M<seconds>S` (par exemple, P2DT5S est un délai de 2 jours, 5 secondes).

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

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> </dl>

 

 





