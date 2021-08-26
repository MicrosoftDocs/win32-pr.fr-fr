---
description: Récupère l’élément suivant de la file d’attente.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Méthode CQueue. GetQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c32039a82e3a0b5c086cbe18e895bdec1aaac09d4947b90d9ba18e8c6636d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108279"
---
# <a name="cqueuegetqueueobject-method"></a>Méthode CQueue. GetQueueObject

Récupère l’élément suivant de la file d’attente.

## <a name="syntax"></a>Syntaxe


```C++
T GetQueueObject();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un objet de type **T** (type de modèle).

## <a name="remarks"></a>Remarques

Cette méthode bloque jusqu’à ce qu’un élément soit disponible dans la file d’attente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CQueue, classe**](cqueue.md)
</dt> </dl>

 

 




