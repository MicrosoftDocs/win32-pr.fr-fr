---
title: TaskSettings. Compatibility, propriété
description: Pour les scripts, obtient ou définit une valeur entière qui indique quelle version de Planificateur de tâches une tâche est compatible.
ms.assetid: bbe21177-e010-4770-9068-9c5b41974ee5
keywords:
- Planificateur de tâches de propriétés de compatibilité
- Planificateur de tâches de propriété de compatibilité, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété de compatibilité
topic_type:
- apiref
api_name:
- TaskSettings.Compatibility
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ba93d3716a8fb0e701cc783ec83abba40190d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740813"
---
# <a name="tasksettingscompatibility-property"></a>TaskSettings. Compatibility, propriété

Pour les scripts, obtient ou définit une valeur entière qui indique quelle version de Planificateur de tâches une tâche est compatible.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.Compatibility As Integer
```



## <a name="property-value"></a>Valeur de la propriété



| Valeur                                                                                                                                                                                                                                         | Signification                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="TASK_COMPATIBILITY_AT"></span><span id="task_compatibility_at"></span><dl> <dt>**Tâche \_ COMPATIBILITÉ \_ à**</dt> <dt>0</dt> </dl> | La tâche est compatible avec la commande AT.<br/>     |
| <span id="TASK_COMPATIBILITY_V1"></span><span id="task_compatibility_v1"></span><dl> <dt>**Tâche \_ COMPATIBILITÉ \_ v1**</dt> <dt>1</dt> </dl> | La tâche est compatible avec Planificateur de tâches 1,0.<br/> |
| <span id="TASK_COMPATIBILITY_V2"></span><span id="task_compatibility_v2"></span><dl> <dt>**Tâche \_ COMPATIBILITÉ \_ v2**</dt> <dt>2</dt> </dl> | La tâche est compatible avec Planificateur de tâches 2,0.<br/> |



 

## <a name="remarks"></a>Notes

La compatibilité des tâches, définie par la propriété de [**compatibilité**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , doit uniquement être définie sur \_ compatibilité \_ des tâches v1 si une tâche doit être accessible ou modifiée à partir d’un ordinateur Windows XP, Windows Server 2003 ou Windows 2000. Dans le cas contraire, il est recommandé d’utiliser la compatibilité Planificateur de tâches 2,0, car la tâche aura davantage de fonctionnalités.

Les tâches compatibles avec la commande AT ne peuvent avoir qu’un seul déclencheur d’heure.

Les tâches compatibles avec Planificateur de tâches 1,0 peuvent uniquement avoir un déclencheur d’heure, un déclencheur de connexion ou un déclencheur de démarrage, et la tâche ne peut avoir qu’une action exécutable.

Pour plus d’informations sur la compatibilité des tâches, consultez [Nouveautés des planificateur de tâches](what-s-new-in-task-scheduler.md) et des [tâches](tasks.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**compatibilité des tâches \_**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





