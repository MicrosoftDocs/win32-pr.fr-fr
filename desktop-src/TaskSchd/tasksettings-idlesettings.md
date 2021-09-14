---
title: TaskSettings. IdleSettings, propriété
description: Pour les scripts, obtient ou définit les informations qui spécifient la façon dont le Planificateur de tâches exécute des tâches lorsque l’ordinateur est dans une condition d’inactivité.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- Planificateur de tâches de la propriété IdleSettings
- Planificateur de tâches de la propriété IdleSettings, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété IdleSettings
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920179"
---
# <a name="tasksettingsidlesettings-property"></a>TaskSettings. IdleSettings, propriété

Pour les scripts, obtient ou définit les informations qui spécifient la façon dont le Planificateur de tâches exécute des tâches lorsque l’ordinateur est dans une condition d’inactivité. Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**IdleSettings**](idlesettings.md) qui spécifie la façon dont le planificateur de tâches gère la tâche lorsque l’ordinateur passe en état d’inactivité.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) du schéma planificateur de tâches.

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

 

 





