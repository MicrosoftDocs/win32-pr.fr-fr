---
title: WeeklyTrigger. RandomDelay, propriété
description: Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur. | WeeklyTrigger. RandomDelay, propriété
ms.assetid: 711b188d-b283-4c99-b43d-644f39a31cdc
keywords:
- Planificateur de tâches de la propriété RandomDelay
- Planificateur de tâches de la propriété RandomDelay, objet WeeklyTrigger
- Planificateur de tâches objet WeeklyTrigger, propriété RandomDelay
topic_type:
- apiref
api_name:
- WeeklyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc17260b33b4f5ca833ae0f2e322a99205b690ad8d54779ea6471db246cc056b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001777"
---
# <a name="weeklytriggerrandomdelay-property"></a>WeeklyTrigger. RandomDelay, propriété

Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.

## <a name="syntax"></a>Syntaxe


```VB
WeeklyTrigger.RandomDelay As String
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



 

 





