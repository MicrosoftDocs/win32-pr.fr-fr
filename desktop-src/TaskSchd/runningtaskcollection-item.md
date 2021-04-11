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
ms.openlocfilehash: 49d28da7a3f5348ff9f5d6171a1a698d95b646f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104650"
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

## <a name="remarks"></a>Notes

Les collections sont de base 1. En d’autres termes, l’index du premier élément de la collection est 1.

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

 

 





