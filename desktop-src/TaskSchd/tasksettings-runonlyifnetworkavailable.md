---
title: TaskSettings. RunOnlyIfNetworkAvailable, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.
ms.assetid: 1a2b085f-0572-47d3-ac1f-0032c8427af0
keywords:
- Planificateur de tâches de la propriété RunOnlyIfNetworkAvailable
- Planificateur de tâches de la propriété RunOnlyIfNetworkAvailable, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété RunOnlyIfNetworkAvailable
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfNetworkAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8225d836e5bc87abd5ce9b6c311b4af527561d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844061"
---
# <a name="tasksettingsrunonlyifnetworkavailable-property"></a>TaskSettings. RunOnlyIfNetworkAvailable, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.RunOnlyIfNetworkAvailable As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est true, la propriété indique que le Planificateur de tâches exécutera la tâche uniquement lorsqu’un réseau est disponible. La valeur par défaut est False.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) du schéma planificateur de tâches.

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

 

 





