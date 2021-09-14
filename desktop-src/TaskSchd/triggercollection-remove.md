---
title: TriggerCollection. Remove, méthode
description: Pour les scripts, supprime le déclencheur spécifié de la collection de déclencheurs utilisée par la tâche.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- déclenche Planificateur de tâches, suppression
- Supprimer la méthode Planificateur de tâches
- Remove, méthode Planificateur de tâches, objet TriggerCollection
- Objet TriggerCollection Planificateur de tâches, Remove, méthode
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857217"
---
# <a name="triggercollectionremove-method"></a>TriggerCollection. Remove, méthode

Pour les scripts, supprime le déclencheur spécifié de la collection de déclencheurs utilisée par la tâche.

## <a name="syntax"></a>Syntaxe


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*index* \[ dans\]
</dt> <dd>

Index du déclencheur à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Lorsque vous supprimez des éléments, Notez que l’index du premier élément de la collection est 1 et que l’index du dernier élément est la valeur de la propriété [**TriggerCollection. Count**](triggercollection-count.md) .

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

 

 





