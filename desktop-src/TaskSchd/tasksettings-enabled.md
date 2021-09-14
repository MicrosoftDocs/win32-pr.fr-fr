---
title: TaskSettings. Enabled, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche est activée. La tâche ne peut être exécutée que lorsque ce paramètre a la valeur true.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Planificateur de tâches de la propriété Enabled
- Propriété Enabled Planificateur de tâches, objet TaskSettings
- Objet TaskSettings Planificateur de tâches, propriété Enabled
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920183"
---
# <a name="tasksettingsenabled-property"></a>TaskSettings. Enabled, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique que la tâche est activée. La tâche ne peut être exécutée que lorsque ce paramètre a la valeur true.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est true, la tâche est activée. Si la valeur est false, la tâche n’est pas activée.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) du schéma planificateur de tâches.

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

 

 





