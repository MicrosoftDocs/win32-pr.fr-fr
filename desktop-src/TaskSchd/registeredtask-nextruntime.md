---
title: RegisteredTask. NextRunTime, propriété
description: Pour les scripts, obtient l’heure à laquelle la tâche inscrite est planifiée pour s’exécuter.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Planificateur de tâches de la propriété NextRunTime
- Planificateur de tâches de la propriété NextRunTime, objet RegisteredTask
- Planificateur de tâches objet RegisteredTask, propriété NextRunTime
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 850c0215555fd24b729b1d71acaff9fa7083c0f53289f28e4228b8e57ff40e52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060047"
---
# <a name="registeredtasknextruntime-property"></a>RegisteredTask. NextRunTime, propriété

Pour les scripts, obtient l’heure à laquelle la tâche inscrite est planifiée pour s’exécuter.

## <a name="syntax"></a>Syntaxe


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>Valeur de la propriété

Heure de la prochaine planification de l’exécution de la tâche inscrite.

## <a name="remarks"></a>Remarques

Si la tâche inscrite contient des déclencheurs qui sont désactivés individuellement, ces déclencheurs affectent toujours la prochaine exécution planifiée retournée même si elles sont désactivées.

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

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





