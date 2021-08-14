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
ms.openlocfilehash: aa405ce4090a080106ec030acbe0ca7211b1c6f94e5874729226ce6adfafa652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760076"
---
# <a name="idlesettingsrestartonidle-property"></a>IdleSettings. RestartOnIdle, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique si la tâche est redémarrée lorsque l’ordinateur est à plusieurs reprises dans une condition d’inactivité.

## <a name="syntax"></a>Syntaxe


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Valeur booléenne qui indique si la tâche doit être redémarrée lorsque l’ordinateur entre dans une condition d’inactivité plusieurs fois. La valeur par défaut est False.

## <a name="remarks"></a>Remarques

Cette propriété est utilisée uniquement si la propriété [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md) a la valeur true.

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) du schéma planificateur de tâches.

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
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

 





