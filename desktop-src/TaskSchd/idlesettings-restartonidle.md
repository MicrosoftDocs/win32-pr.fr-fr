---
title: IdleSettings. RestartOnIdle, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique si la tâche est redémarrée lorsque l’ordinateur est à plusieurs reprises dans une condition d’inactivité.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Planificateur de tâches de la propriété RestartOnIdle
- Planificateur de tâches de la propriété RestartOnIdle, objet IdleSettings
- Planificateur de tâches objet IdleSettings, propriété RestartOnIdle
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543052"
---
# <a name="idlesettingsrestartonidle-property"></a>IdleSettings. RestartOnIdle, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique si la tâche est redémarrée lorsque l’ordinateur est à plusieurs reprises dans une condition d’inactivité.

## <a name="syntax"></a>Syntaxe


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Valeur booléenne qui indique si la tâche doit être redémarrée lorsque l’ordinateur entre dans une condition d’inactivité plusieurs fois. La valeur par défaut est False.

## <a name="remarks"></a>Notes

Cette propriété est utilisée uniquement si la propriété [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md) a la valeur true.

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) du schéma planificateur de tâches.

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
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





