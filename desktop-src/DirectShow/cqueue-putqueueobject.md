---
description: Place un élément dans la file d’attente.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: Méthode CQueue. PutQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6e3539b12f81421e90de1f8311210aa2acb77173be2991bd6f15a1c84d39ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539009"
---
# <a name="cqueueputqueueobject-method"></a>Méthode CQueue. PutQueueObject

Place un élément dans la file d’attente.

## <a name="syntax"></a>Syntaxe


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*object* 
</dt> <dd>

Objet de type **T** (type de modèle).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode bloque jusqu’à ce qu’il y ait de l’espace dans la file d’attente pour l’élément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CQueue, classe**](cqueue.md)
</dt> </dl>

 

 




