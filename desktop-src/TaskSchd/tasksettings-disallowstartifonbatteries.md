---
title: TaskSettings. DisallowStartIfOnBatteries, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- Planificateur de tâches de la propriété DisallowStartIfOnBatteries
- Planificateur de tâches de la propriété DisallowStartIfOnBatteries, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105346"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a>TaskSettings. DisallowStartIfOnBatteries, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Valeur booléenne qui indique que la tâche ne sera pas démarrée si l’ordinateur fonctionne sur batterie. Si la valeur est true, la tâche n’est pas démarrée si l’ordinateur fonctionne sur batterie. Si la valeur est false, la tâche est démarrée si l’ordinateur fonctionne sur batterie. La valeur par défaut est True.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) du schéma planificateur de tâches.

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

 

 





