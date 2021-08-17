---
title: RegisteredTaskCollection. Item, propriété
description: Pour les scripts, obtient la tâche inscrite spécifiée à partir de la collection.
ms.assetid: 8b396478-4cd9-426c-afe8-29539ff0b859
keywords:
- Planificateur de tâches de propriété d’élément
- Propriété Item Planificateur de tâches, objet RegisteredTaskCollection
- Objet RegisteredTaskCollection Planificateur de tâches, propriété Item
topic_type:
- apiref
api_name:
- RegisteredTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fff69074bb650cf3bc639051118b71db6d40678c3ac055e589d318ef45fff3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253519"
---
# <a name="registeredtaskcollectionitem-property"></a>RegisteredTaskCollection. Item, propriété

Pour les scripts, obtient la tâche inscrite spécifiée à partir de la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
RegisteredTaskCollection.Item( _
  ByVal Index _
) As RegisteredTask
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**RegisteredTask**](registeredtask.md) qui contient la tâche inscrite.

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

 

 





