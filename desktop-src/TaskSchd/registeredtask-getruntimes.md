---
title: Méthode RegisteredTask. GetRunTimes
description: Pour les scripts, obtient le nombre de fois que la tâche inscrite est planifiée pour s’exécuter pendant une période spécifiée.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Planificateur de tâches de la méthode GetRunTimes
- Méthode GetRunTimes Planificateur de tâches, objet RegisteredTask
- Planificateur de tâches objet RegisteredTask, méthode GetRunTimes
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c15aba82c5515578a3c58a485e47718d09176483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509058"
---
# <a name="registeredtaskgetruntimes-method"></a>Méthode RegisteredTask. GetRunTimes

Pour les scripts, obtient le nombre de fois que la tâche inscrite est planifiée pour s’exécuter pendant une période spécifiée.

## <a name="syntax"></a>Syntaxe


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*commencer* \[ dans\]
</dt> <dd>

Heure de début de la requête.

</dd> <dt>

*fin* \[ dans\]
</dt> <dd>

Heure de fin de la requête.

</dd> <dt>

*nombre* \[ à\]
</dt> <dd>

Nombre de fois que la tâche est exécutée.

</dd> <dt>

*rgstTaskTimes* \[ à\]
</dt> <dd>

Heures planifiées d’exécution de la tâche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si la tâche inscrite contient des déclencheurs qui sont désactivés individuellement, ces déclencheurs affectent toujours la prochaine exécution planifiée retournée même si elles sont désactivées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





