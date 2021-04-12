---
title: ActionCollection. Item, propriété
description: Pour les scripts, obtient une action spécifiée à partir de la collection.
ms.assetid: a5567c82-2d56-4c3e-894c-ca6d432a3358
keywords:
- Planificateur de tâches de propriété d’élément
- Propriété Item Planificateur de tâches, objet ActionCollection
- Objet ActionCollection Planificateur de tâches, propriété Item
topic_type:
- apiref
api_name:
- ActionCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4853009c547f3bdfbb269e512ce5d39273726095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385012"
---
# <a name="actioncollectionitem-property"></a>ActionCollection. Item, propriété

Pour les scripts, obtient une action spécifiée à partir de la collection.

## <a name="syntax"></a>Syntaxe


```VB
ActionCollection.Item( _
  ByVal Index _
) As Action
```



## <a name="property-value"></a>Valeur de la propriété

Objet d' [**action**](action.md) qui représente l’action demandée.

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
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> </dl>

 

 





