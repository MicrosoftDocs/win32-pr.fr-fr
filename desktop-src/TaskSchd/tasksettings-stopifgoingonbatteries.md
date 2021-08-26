---
title: TaskSettings. StopIfGoingOnBatteries, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche sera arrêtée si l’ordinateur est sur batteries.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- Planificateur de tâches de la propriété StopIfGoingOnBatteries
- Planificateur de tâches de la propriété StopIfGoingOnBatteries, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229d5d3beef974e9ce8758f9bd81fc3217bd9c3fcf9bf37be137abe6515cc62a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974885"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a>TaskSettings. StopIfGoingOnBatteries, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche sera arrêtée si l’ordinateur est sur batteries.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Valeur booléenne qui indique que la tâche sera arrêtée si l’ordinateur passe sur batteries. Si la valeur est true, la propriété indique que la tâche sera arrêtée si l’ordinateur passe sur batteries. Si la valeur est false, la propriété indique que la tâche ne sera pas arrêtée si l’ordinateur passe sur batteries. La valeur par défaut est True. Pour plus d’informations, consultez la section Notes.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) du schéma planificateur de tâches.

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

 

 





