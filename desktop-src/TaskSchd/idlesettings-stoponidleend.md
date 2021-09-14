---
title: IdleSettings. StopOnIdleEnd, propriété
description: Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches met fin à la tâche si la condition d’inactivité se termine avant la fin de la tâche.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- Planificateur de tâches de la propriété StopOnIdleEnd
- Planificateur de tâches de la propriété StopOnIdleEnd, objet IdleSettings
- Planificateur de tâches objet IdleSettings, propriété StopOnIdleEnd
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013444"
---
# <a name="idlesettingsstoponidleend-property"></a>IdleSettings. StopOnIdleEnd, propriété

Pour les scripts, obtient ou définit une valeur booléenne qui indique que le Planificateur de tâches met fin à la tâche si la condition d’inactivité se termine avant la fin de la tâche.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Valeur booléenne qui indique que la Planificateur de tâches met fin à la tâche si la condition d’inactivité se termine avant la fin de la tâche.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de données XML pour une tâche, ce paramètre est spécifié dans l’élément [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) du schéma planificateur de tâches.

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

 

 





