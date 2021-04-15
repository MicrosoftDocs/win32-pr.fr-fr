---
title: TaskSettings. RestartCount, propriété
description: Pour les scripts, obtient ou définit le nombre de fois que l’Planificateur de tâches tente de redémarrer la tâche.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- Planificateur de tâches de la propriété RestartCount
- Planificateur de tâches de la propriété RestartCount, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété RestartCount
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee033eebde7b085d6df40f1e5e20d6dcf640a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384344"
---
# <a name="tasksettingsrestartcount-property"></a>TaskSettings. RestartCount, propriété

Pour les scripts, obtient ou définit le nombre de fois que l’Planificateur de tâches tente de redémarrer la tâche.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a>Valeur de la propriété

Nombre de tentatives de redémarrage de la tâche par le Planificateur de tâches.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Count**](taskschedulerschema-count-restarttype-element.md) du schéma planificateur de tâches.

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

 

 





