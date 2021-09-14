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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920204"
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

## <a name="requirements"></a>Spécifications



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

 

 





