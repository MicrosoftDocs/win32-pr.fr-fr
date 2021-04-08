---
title: RunningTask. State, propriété
description: Pour les scripts, obtient un identificateur pour l’état de la tâche en cours d’exécution.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- Planificateur de tâches de propriété d’État
- Propriété State Planificateur de tâches, objet RunningTask
- Objet RunningTask Planificateur de tâches, propriété State
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b962de116eef1301be209828181147dfe03273e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740853"
---
# <a name="runningtaskstate-property"></a>RunningTask. State, propriété

Pour les scripts, obtient un identificateur pour l’état de la tâche en cours d’exécution.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
RunningTask.State As String
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur de l’état de la tâche en cours d’exécution.



| Valeur                                                                                                                                                                                                                                   | Signification                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**Tâche \_ ÉTAT \_ inconnu**</dt> <dt>0</dt> </dl>    | L’état de la tâche est inconnu.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**Tâche \_ ÉTAT \_ désactivé**</dt> <dt>1</dt> </dl> | La tâche est inscrite, mais elle est désactivée et aucune instance de la tâche n’est mise en file d’attente ou en cours d’exécution. La tâche ne peut pas être exécutée tant qu’elle n’est pas activée.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**Tâche \_ État en \_ file d’attente**</dt> <dt>2</dt> </dl>       | Les instances de la tâche sont mises en file d’attente.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**Tâche \_ ÉTAT \_ prêt**</dt> <dt>3</dt> </dl>          | La tâche est prête à être exécutée, mais aucune instance n’est en file d’attente ou en cours d’exécution.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**Tâche \_ ÉTAT \_ en cours d’exécution**</dt> <dt>4</dt> </dl>    | Une ou plusieurs instances de la tâche sont en cours d’exécution.<br/>                                                                                         |



 

## <a name="remarks"></a>Notes

La méthode [**RunningTask. Refresh**](runningtask-refresh.md) est appelée avant que la valeur de la propriété ne soit retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





