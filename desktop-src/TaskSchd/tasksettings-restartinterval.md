---
title: TaskSettings. RestartInterval, propriété
description: Pour les scripts, obtient ou définit une valeur qui spécifie la durée pendant laquelle l’Planificateur de tâches tente de redémarrer la tâche.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Planificateur de tâches de la propriété RestartInterval
- Planificateur de tâches de la propriété RestartInterval, objet TaskSettings
- Planificateur de tâches objet TaskSettings, propriété RestartInterval
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3293072fcec50b140a298887b12ed8f5dd1fb6a298c3b486069fe2e7eccaef00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681609"
---
# <a name="tasksettingsrestartinterval-property"></a>TaskSettings. RestartInterval, propriété

Pour les scripts, obtient ou définit une valeur qui spécifie la durée pendant laquelle l’Planificateur de tâches tente de redémarrer la tâche.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a>Valeur de la propriété

Valeur qui spécifie la durée pendant laquelle l’Planificateur de tâches tente de redémarrer la tâche. Si cette propriété est définie, la propriété [**RestartCount**](tasksettings-restartcount.md) doit également être définie. Le format de cette chaîne est `P<days>DT<hours>H<minutes>M<seconds>S` (par exemple, « PT5M » est de 5 minutes, « PT1H » est 1 heure et « PT20M » est 20 minutes). La durée maximale autorisée est de 31 jours, et la durée minimale autorisée est de 1 minute.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**Interval**](taskschedulerschema-interval-restarttype-element.md) du schéma planificateur de tâches.

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

 

 





