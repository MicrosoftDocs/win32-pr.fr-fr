---
description: Nombre de mémoires tampons à fournir.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Membre CBaseAllocator :: m_lCount (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c33749ee6293c301501962939e25118595db10592713fb46dc10d01083c0096f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661691"
---
# <a name="cbaseallocatorm_lcount-member"></a>CBaseAllocator :: m \_ lCount, membre

Nombre de mémoires tampons à fournir. La méthode [**CBaseAllocator :: SetProperties**](cbaseallocator-setproperties.md) définit cette valeur. Les mémoires tampons ne sont pas allouées tant que la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) n’est pas appelée. Le nombre actuel de mémoires tampons allouées est spécifié par la variable de membre [**CBaseAllocator :: m \_ lAllocated**](cbaseallocator-m-lallocated.md) .

## <a name="syntax"></a>Syntaxe


```C++
long m_lCount;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseAllocator, classe**](cbaseallocator.md)
</dt> </dl>

 

 




