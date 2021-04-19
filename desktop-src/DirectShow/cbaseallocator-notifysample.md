---
description: La méthode NotifySample libère tous les threads qui attendent des exemples.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Méthode CBaseAllocator. NotifySample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541696"
---
# <a name="cbaseallocatornotifysample-method"></a>Méthode CBaseAllocator. NotifySample

La `NotifySample` méthode libère tous les threads qui attendent des exemples.

## <a name="syntax"></a>Syntaxe


```C++
void NotifySample();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Quand des threads attendent des exemples, la valeur de [**CBaseAllocator :: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) est supérieure à zéro. Si *m \_ lWaiting* est supérieur à zéro, cette méthode appelle la fonction **ReleaseSemaphore,** sur le sémaphore [**CBaseAllocator :: m \_ hSem**](cbaseallocator-m-hsem.md) , en activant tous les threads en attente. Elle réinitialise également *m \_ lWaiting* à zéro.

Cette méthode est appelée à partir de la méthode [**CBaseAllocator :: ReleaseBuffer**](cbaseallocator-releasebuffer.md) , lorsqu’un exemple est retourné à la liste libre ; et à partir de la méthode [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) , lorsque l’allocation est désallouée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




