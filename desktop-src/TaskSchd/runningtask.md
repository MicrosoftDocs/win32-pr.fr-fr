---
title: Objet RunningTask
description: Objet de script qui fournit les méthodes permettant d’obtenir des informations et de contrôler une tâche en cours d’exécution.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- Objet RunningTask Planificateur de tâches
- Planificateur de tâches d’objets RunningTask, Description
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508862"
---
# <a name="runningtask-object"></a>Objet RunningTask

Objet de script qui fournit les méthodes permettant d’obtenir des informations et de contrôler une tâche en cours d’exécution.

## <a name="members"></a>Membres

L’objet **RunningTask** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **RunningTask** a ces méthodes.



| Méthode                                 | Description                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [**Actualiser**](runningtask-refresh.md) | Actualise toutes les variables d’instance locales de la tâche.<br/> |
| [**Erreur**](runningtask-stop.md)       | Arrête cette instance de la tâche.<br/>                           |



 

### <a name="properties"></a>Propriétés

L’objet **RunningTask** a ces propriétés.



| Propriété                                                      | Type d’accès          | Description                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**CurrentAction**](runningtask-currentaction.md)<br/> | Lecture seule<br/> | Obtient le nom de l’action en cours exécutée par la tâche en cours d’exécution.<br/> |
| [**EnginePID**](runningtask-enginepid.md)<br/>         | Lecture seule<br/> | Obtient l’ID de processus pour le moteur (processus) qui exécute la tâche.<br/>  |
| [**InstanceGuid**](runningtask-instanceguid.md)<br/>   | Lecture seule<br/> | Obtient l’identificateur GUID de cette instance de la tâche.<br/>                  |
| [**Nom**](runningtask-name.md)<br/>                   | Lecture seule<br/> | Obtient le nom de la tâche.<br/>                                               |
| [**D**](runningtask-path.md)<br/>                   | Lecture seule<br/> | Obtient le chemin d’accès à l’emplacement où la tâche est stockée.<br/>                               |
| [**State**](runningtask-state.md)<br/>                 | Lecture seule<br/> | Obtient l’état de la tâche en cours d’exécution. <br/>                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Planificateur de tâches](task-scheduler-objects.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**RunningTaskCollection**](runningtaskcollection.md)
</dt> <dt>

[**RegisteredTask. Run**](registeredtask-run.md)
</dt> <dt>

[**RegisteredTask.RunEx**](registeredtask-runex.md)
</dt> </dl>

 

 





