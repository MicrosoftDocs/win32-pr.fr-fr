---
title: TaskSettings. Priority (propriété)
description: Pour les scripts, obtient ou définit le niveau de priorité de la tâche.
ms.assetid: 2548fcb6-c649-4822-a2ea-77546aac2ec5
keywords:
- Planificateur de tâches de la propriété Priority
- Propriété Priority Planificateur de tâches, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété Priority
topic_type:
- apiref
api_name:
- TaskSettings.Priority
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b24c0281e8df314b070e0569176899b96071e1ef43caab17af4978e74f6b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354826"
---
# <a name="tasksettingspriority-property"></a>TaskSettings. Priority (propriété)

Pour les scripts, obtient ou définit le niveau de priorité de la tâche.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.Priority As Integer
```



## <a name="property-value"></a>Valeur de la propriété

Niveau de priorité (0-10) de la tâche. La valeur par défaut est 7.

## <a name="remarks"></a>Remarques

Le niveau de priorité 0 est la priorité la plus élevée et le niveau de priorité 10 est la priorité la plus basse. La valeur par défaut est 7. Les niveaux de priorité 7 et 8 sont utilisés pour les tâches en arrière-plan, et les niveaux de priorité 4, 5 et 6 sont utilisés pour les tâches interactives.

L’action de la tâche est démarrée dans un processus avec une priorité basée sur une valeur de classe de priorité. Une valeur de niveau de priorité (priorité de thread) est utilisée pour les actions de la tâche du gestionnaire COM, de la boîte de message et de l’e-mail. Pour plus d’informations sur la classe de priorité et les valeurs de niveau de priorité, consultez [planification des priorités](/windows/desktop/ProcThread/scheduling-priorities). Le tableau suivant répertorie les valeurs possibles pour le paramètre *Priority* et les valeurs de classe de priorité et de niveau de priorité correspondantes.



| *Priorité* de la tâche | Classe de priorité                 | Niveau de priorité                   |
|-----------------|--------------------------------|----------------------------------|
| 0               | \_classe de priorité en temps réel \_      | temps de priorité des THREADs \_ \_ \_ critique |
| 1               | \_classe de priorité élevée \_          | priorité de THREAD la \_ \_ plus élevée        |
| 2               | classe de priorité supérieure à la \_ normale \_ \_ | priorité de THREAD supérieure à la \_ \_ \_ normale  |
| 3               | classe de priorité supérieure à la \_ normale \_ \_ | priorité de THREAD supérieure à la \_ \_ \_ normale  |
| 4               | \_classe de priorité normale \_        | priorité de THREAD \_ \_ normale         |
| 5               | \_classe de priorité normale \_        | priorité de THREAD \_ \_ normale         |
| 6               | \_classe de priorité normale \_        | priorité de THREAD \_ \_ normale         |
| 7               | classe de priorité inférieure à la \_ normale \_ \_ | priorité de THREAD inférieure à la \_ \_ \_ normale  |
| 8               | classe de priorité inférieure à la \_ normale \_ \_ | priorité de THREAD inférieure à la \_ \_ \_ normale  |
| 9               | \_classe de priorité Idle \_          | priorité de THREAD la \_ \_ plus basse         |
| 10              | \_classe de priorité Idle \_          | priorité de THREAD \_ \_ inactive           |



 

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> </dl>

 

