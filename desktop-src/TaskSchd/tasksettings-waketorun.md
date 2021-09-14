---
title: TaskSettings. WakeToRun, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- Planificateur de tâches de la propriété WakeToRun
- Planificateur de tâches de la propriété WakeToRun, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété WakeToRun
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013403"
---
# <a name="tasksettingswaketorun-property"></a>TaskSettings. WakeToRun, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntax


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la valeur est true, la propriété indique que la Planificateur de tâches met l’ordinateur en éveil lorsqu’il est temps d’exécuter la tâche.

## <a name="remarks"></a>Notes

Lorsque le service Planificateur de tâches sort de l’ordinateur pour exécuter une tâche, l’écran peut rester inactif même si l’ordinateur n’est plus en mode veille ou veille prolongée. l’écran s’active quand Windows Vista détecte qu’un utilisateur est revenu à utiliser l’ordinateur.

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) du schéma planificateur de tâches.

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

 

 





