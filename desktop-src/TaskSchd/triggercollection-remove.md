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
ms.openlocfilehash: d1ff3fda5119f4b487ba7f04546ea94e0a601a4749e1aa6aad7a9120907cd6cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099642"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Lorsque vous supprimez des éléments, Notez que l’index du premier élément de la collection est 1 et que l’index du dernier élément est la valeur de la propriété [**TriggerCollection. Count**](triggercollection-count.md) .

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

 

 





