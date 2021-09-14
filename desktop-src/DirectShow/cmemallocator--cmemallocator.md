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
ms.openlocfilehash: 43b0505ee34df72ab82e4204b08440ac1a2558b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195628"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>CMemAllocator. ~ CMemAllocator, destructeur

Méthode de destructeur.

## <a name="syntax"></a>Syntaxe


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Notes

Cette méthode remplace le destructeur de classe de base pour appeler [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) et [**CMemAllocator :: ReallyFree**](cmemallocator-reallyfree.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMemAllocator, classe**](cmemallocator.md)
</dt> </dl>

 

 




