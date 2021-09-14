---
title: TriggerCollection. Item, propriété
description: Pour les scripts, obtient le déclencheur spécifié à partir de la collection.
ms.assetid: 517976df-b3fc-4f2e-8d37-262195c65182
keywords:
- Planificateur de tâches de propriété d’élément
- Propriété Item Planificateur de tâches, objet TriggerCollection
- Objet TriggerCollection Planificateur de tâches, propriété Item
topic_type:
- apiref
api_name:
- TriggerCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d600418d43459d6c4cbfcb0746a378633d096c24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857218"
---
# <a name="triggercollectionitem-property"></a>TriggerCollection. Item, propriété

Pour les scripts, obtient le déclencheur spécifié à partir de la collection.

## <a name="syntax"></a>Syntaxe


```VB
TriggerCollection.Item( _
  ByVal index _
) As Trigger
```



## <a name="property-value"></a>Valeur de la propriété

Objet de [**déclencheur**](trigger.md) qui représente le déclencheur demandé.

## <a name="remarks"></a>Notes

Les collections sont de base 1. En d’autres termes, l’index du premier élément de la collection est 1.

## <a name="requirements"></a>Spécifications



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

 

 





