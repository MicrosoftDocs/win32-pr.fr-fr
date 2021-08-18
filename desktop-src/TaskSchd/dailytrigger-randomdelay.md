---
title: DailyTrigger. RandomDelay, propriété
description: Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur. | DailyTrigger. RandomDelay, propriété
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- Planificateur de tâches de la propriété RandomDelay
- Planificateur de tâches de la propriété RandomDelay, objet DailyTrigger
- Planificateur de tâches objet DailyTrigger, propriété RandomDelay
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc3bfec997b50a1f9d802191387a2186576532ca027e1086fc311b31f0da5d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139472"
---
# <a name="dailytriggerrandomdelay-property"></a>DailyTrigger. RandomDelay, propriété

Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.

## <a name="syntax"></a>Syntaxe


```VB
DailyTrigger.RandomDelay As String
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

[**DailyTrigger**](dailytrigger.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





