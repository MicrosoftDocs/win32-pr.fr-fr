---
title: TaskNamedValueCollection. Item, propriété
description: Pour les scripts, obtient la paire nom-valeur spécifiée à partir de la collection.
ms.assetid: 89c87b22-e459-435d-8c15-69907e9b1329
keywords:
- Planificateur de tâches de propriété d’élément
- Propriété Item Planificateur de tâches, objet TaskNamedValueCollection
- Objet TaskNamedValueCollection Planificateur de tâches, propriété Item
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55dd6479486bb481f31e7aaf2b920ef591d1fa1019d432b22568fa7d7f56bf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991469"
---
# <a name="tasknamedvaluecollectionitem-property"></a>TaskNamedValueCollection. Item, propriété

Pour les scripts, obtient la paire nom-valeur spécifiée à partir de la collection.

## <a name="syntax"></a>Syntaxe


```VB
TaskNamedValueCollection.Item( _
  ByVal index, _
  ByRef pair _
) As long
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**TaskNamedValuePair**](tasknamedvaluepair.md) qui représente la paire demandée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





