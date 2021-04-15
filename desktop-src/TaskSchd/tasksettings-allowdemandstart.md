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
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384091"
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

## <a name="remarks"></a>Notes

Lorsque cette propriété a la valeur true, la tâche peut être démarrée indépendamment de la date à laquelle les déclencheurs démarrent la tâche.

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) du schéma planificateur de tâches.

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

 

 





