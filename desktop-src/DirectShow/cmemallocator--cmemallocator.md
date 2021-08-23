---
description: CMemAllocator. ~ CMemAllocator, destructeur, méthode de destructeur.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: CMemAllocator. ~ CMemAllocator, destructeur (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 588b370fc56f6af547ead19c7a52758a3851dd7e46d88b90f8f621ed6002d6e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954378"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>CMemAllocator. ~ CMemAllocator, destructeur

Méthode de destructeur.

## <a name="syntax"></a>Syntaxe


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Notes

Cette méthode remplace le destructeur de classe de base pour appeler [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) et [**CMemAllocator :: ReallyFree**](cmemallocator-reallyfree.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMemAllocator, classe**](cmemallocator.md)
</dt> </dl>

 

 




