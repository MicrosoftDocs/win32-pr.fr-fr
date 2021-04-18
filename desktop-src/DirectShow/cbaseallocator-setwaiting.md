---
description: La méthode SetWaiting incrémente le nombre de threads en attente.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Méthode CBaseAllocator. SetWaiting (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526413"
---
# <a name="cbaseallocatorsetwaiting-method"></a>Méthode CBaseAllocator. SetWaiting

La `SetWaiting` méthode incrémente le nombre de threads en attente.

## <a name="syntax"></a>Syntaxe


```C++
void SetWaiting();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode incrémente la variable membre [**CBaseAllocator :: m \_ lWaiting**](cbaseallocator-m-lwaiting.md) . Si un thread est bloqué dans la méthode [**CBaseAllocator :: GetBuffer**](cbaseallocator-getbuffer.md) , l’allocateur appelle, `SetWaiting` puis attend que le sémaphore [**CBaseAllocator :: m \_ hSem**](cbaseallocator-m-hsem.md) soit signalé. La méthode [**CBaseAllocator :: ReleaseBuffer**](cbaseallocator-releasebuffer.md) signale le sémaphore et définit la valeur de *m \_ lWaiting* sur zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




