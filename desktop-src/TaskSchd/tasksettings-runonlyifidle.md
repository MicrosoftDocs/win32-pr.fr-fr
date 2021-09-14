---
title: TaskSettings. RunOnlyIfIdle, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches exécutera la tâche uniquement si l’ordinateur est dans une condition d’inactivité.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Planificateur de tâches de la propriété RunOnlyIfIdle
- Planificateur de tâches de la propriété RunOnlyIfIdle, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété RunOnlyIfIdle
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095638"
---
# <a name="tasksettingsrunonlyifidle-property"></a>TaskSettings. RunOnlyIfIdle, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches exécutera la tâche uniquement si l’ordinateur est dans une condition d’inactivité.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est true, la propriété indique que le Planificateur de tâches exécutera la tâche uniquement si l’ordinateur est dans une condition d’inactivité. La valeur par défaut est False.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) du schéma planificateur de tâches.

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

 

 





