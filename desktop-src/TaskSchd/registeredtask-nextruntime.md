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
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122933"
---
# <a name="registeredtasknextruntime-property"></a>RegisteredTask. NextRunTime, propriété

Pour les scripts, obtient l’heure à laquelle la tâche inscrite est planifiée pour s’exécuter.

## <a name="syntax"></a>Syntaxe


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>Valeur de la propriété

Heure de la prochaine planification de l’exécution de la tâche inscrite.

## <a name="remarks"></a>Notes

Si la tâche inscrite contient des déclencheurs qui sont désactivés individuellement, ces déclencheurs affectent toujours la prochaine exécution planifiée retournée même si elles sont désactivées.

## <a name="requirements"></a>Spécifications



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

 

 





