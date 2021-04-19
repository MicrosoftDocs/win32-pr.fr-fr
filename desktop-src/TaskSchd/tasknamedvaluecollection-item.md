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
ms.openlocfilehash: 4dd0abff47d699fd6d85f04745f28e2feb31c6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509739"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





