---
title: TaskSettings. StartWhenAvailable, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la Planificateur de tâches peut démarrer la tâche à tout moment une fois que l’heure planifiée est passée.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Planificateur de tâches de la propriété StartWhenAvailable
- Planificateur de tâches de la propriété StartWhenAvailable, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété StartWhenAvailable
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466406"
---
# <a name="tasksettingsstartwhenavailable-property"></a>TaskSettings. StartWhenAvailable, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique que la Planificateur de tâches peut démarrer la tâche à tout moment une fois que l’heure planifiée est passée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est true, la propriété indique que la Planificateur de tâches peut démarrer la tâche à tout moment une fois que l’heure planifiée est passée. La valeur par défaut est False.

## <a name="remarks"></a>Notes

Cette propriété s’applique uniquement aux tâches basées sur le temps avec une limite de fin ou des tâches basées sur le temps qui sont configurées pour se répéter de manière infinie.

Les tâches qui sont démarrées après l’heure planifiée sont passées (en raison de la propriété [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) définie sur true) sont mises en file d’attente dans la file d’attente de tâches du service Planificateur de tâches et elles sont démarrées après un certain délai. Le délai par défaut est de 10 minutes.

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) du schéma planificateur de tâches.

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

 

 





