---
title: TaskSettings. MultipleInstances, propriété
description: Pour les scripts, obtient ou définit la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Planificateur de tâches de la propriété MultipleInstances
- Planificateur de tâches de la propriété MultipleInstances, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété MultipleInstances
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794ea07f1c01dabe957181bd327f8787f873917b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508369"
---
# <a name="tasksettingsmultipleinstances-property"></a>TaskSettings. MultipleInstances, propriété

Pour les scripts, obtient ou définit la stratégie qui définit la façon dont le Planificateur de tâches gère plusieurs instances de la tâche.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a>Valeur de la propriété

[**Tâche \_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) Constantes de stratégie d’instances.



| Valeur                                                                                                                                                                                                                                                               | Signification                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <dt>**Tâche \_ INSTANCES \_ parallèles**</dt> <dt>0</dt> </dl>                 | Démarre une nouvelle instance lorsqu’une instance existante de la tâche est en cours d’exécution.<br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <dt>**Tâche \_ INSTANCES, \_ file d’attente**</dt> <dt>1</dt> </dl>                          | Démarre une nouvelle instance de la tâche une fois que toutes les autres instances de la tâche sont terminées.<br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <dt>**Tâche \_ Les INSTANCES \_ ignorent les \_ nouvelles**</dt> <dt>2</dt> </dl>          | Ne démarre pas une nouvelle instance si une instance existante de la tâche est en cours d’exécution.<br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <dt>**Tâche \_ Arrêter les INSTANCES \_ \_ existantes**</dt> <dt>3</dt> </dl> | Arrête une instance existante de la tâche avant de démarrer une nouvelle instance.<br/>                 |



 

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_stratégie d’instances de tâche \_**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





