---
description: CBaseAllocator. ~ CBaseAllocator, destructeur, méthode de destructeur.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: CBaseAllocator. ~ CBaseAllocator, destructeur (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89b87bd4e706e5270b49ca94d1c86a6c5a5326fd3efccb1dcc45b9681e6e2fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017557"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>CBaseAllocator. ~ CBaseAllocator, destructeur

Méthode de destructeur.

## <a name="syntax"></a>Syntaxe


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Notes

Appelez toujours la méthode [**CBaseAllocator ::D ecommit**](cbaseallocator-decommit.md) avant de détruire l’objet. Le destructeur de classe de base ne peut pas appeler **decommit**, car cette méthode appelle la méthode virtuelle pure [**CBaseAllocator :: Free**](cbaseallocator-free.md). Les classes dérivées doivent substituer ce destructeur et appeler **decommit**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




