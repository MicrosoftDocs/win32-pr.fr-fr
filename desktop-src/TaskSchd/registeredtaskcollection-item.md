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
ms.openlocfilehash: 9ec79eb526b85b88afc0e5747a80b45f07b99a9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511930"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





