---
title: TaskSettings. AllowDemandStart, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Planificateur de tâches de la propriété AllowDemandStart
- Planificateur de tâches de la propriété AllowDemandStart, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété AllowDemandStart
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a48ecaf9010b4269ffff66b556d01cfccc057fd05207f619290af9e50f6c757f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959479"
---
# <a name="tasksettingsallowdemandstart-property"></a>TaskSettings. AllowDemandStart, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est true, la tâche peut être exécutée à l’aide de la commande exécuter ou du menu contextuel. Si la valeur est false, la tâche ne peut pas être exécutée à l’aide de la commande exécuter ou du menu contextuel. La valeur par défaut est True.

## <a name="remarks"></a>Remarques

Lorsque cette propriété a la valeur true, la tâche peut être démarrée indépendamment de la date à laquelle les déclencheurs démarrent la tâche.

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





