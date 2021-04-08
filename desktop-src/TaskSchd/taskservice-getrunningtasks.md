---
title: Méthode TaskService. GetRunningTasks
description: Pour les scripts, obtient une collection de tâches en cours d’exécution.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- Planificateur de tâches de la méthode GetRunningTasks
- Méthode GetRunningTasks Planificateur de tâches, objet TaskService
- Planificateur de tâches objet TaskService, méthode GetRunningTasks
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743740"
---
# <a name="taskservicegetrunningtasks-method"></a>Méthode TaskService. GetRunningTasks

Pour les scripts, obtient une collection de tâches en cours d’exécution.

> [!Note]  
> **TaskService. GetRunningTasks** retourne uniquement une collection de tâches en cours d’exécution qui s’exécutent au-dessous ou au-dessous du contexte de sécurité d’un utilisateur. Par exemple, pour les membres du groupe administrateurs, **GetRunningTasks** retourne une collection de toutes les tâches en cours d’exécution, mais pour les membres du groupe utilisateurs, **GetRunningTasks** renvoie uniquement une collection de tâches qui s’exécutent dans le contexte de sécurité du groupe utilisateurs.

 

## <a name="syntax"></a>Syntaxe


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Transmettez 1 pour retourner toutes les tâches en cours d’exécution, y compris les tâches masquées. Transmettez 0 pour retourner une collection de tâches en cours d’exécution qui ne sont pas des tâches masquées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Objet [**RunningTaskCollection**](runningtaskcollection.md) qui contient les tâches en cours d’exécution.

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
</dt> </dl>

 

 





