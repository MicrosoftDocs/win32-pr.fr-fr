---
title: RunningTaskCollection. Item, propriété
description: Pour les scripts, obtient la tâche spécifiée à partir de la collection.
ms.assetid: 8b0745da-a11f-426c-9d52-f59d188e0e86
keywords:
- Planificateur de tâches de propriété d’élément
- Propriété Item Planificateur de tâches, objet RunningTaskCollection
- Objet RunningTaskCollection Planificateur de tâches, propriété Item
topic_type:
- apiref
api_name:
- RunningTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7e2ca7abf5f1daa936509d5fae71211e8b139537fa1782daac6c08bf9a1017f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866779"
---
# <a name="runningtaskcollectionitem-property"></a>RunningTaskCollection. Item, propriété

Pour les scripts, obtient la tâche spécifiée à partir de la collection.

## <a name="syntax"></a>Syntaxe


```VB
RunningTaskCollection.Item( _
  ByVal Index _
) As RunningTask
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**RunningTask**](runningtask.md) qui contient le contexte demandé.

## <a name="remarks"></a>Remarques

Les collections sont de base 1. En d’autres termes, l’index du premier élément de la collection est 1.

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

 

 





