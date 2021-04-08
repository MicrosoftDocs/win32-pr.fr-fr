---
title: TaskSettings. AllowHardTerminate, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche peut être terminée par le service Planificateur de tâches à l’aide de TerminateProcess.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- Planificateur de tâches de la propriété AllowHardTerminate
- Planificateur de tâches de la propriété AllowHardTerminate, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété AllowHardTerminate
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742413"
---
# <a name="tasksettingsallowhardterminate-property"></a>TaskSettings. AllowHardTerminate, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche peut être terminée par le service Planificateur de tâches à l’aide de [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Le service tente de fermer la tâche en cours d’exécution en envoyant la notification [**WM \_ Close**](../winmsg/wm-close.md) et, si la tâche ne répond pas, la tâche ne se termine que si cette propriété a la valeur true.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est true, la tâche peut être arrêtée à l’aide de [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Si la valeur est false, la tâche ne peut pas être arrêtée à l’aide de **TerminateProcess**.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) du schéma planificateur de tâches.

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

 

