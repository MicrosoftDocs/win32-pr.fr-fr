---
description: Pointeur vers le bloc de mémoire qui contient les mémoires tampons.
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: 'Membre CMemAllocator :: m_pBuffer (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pBuffer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fa9c56c5a90c1fa3fde7dda4bca82cd3f473a591db9e2e24f0b1d141c6aa33e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155981"
---
# <a name="cmemallocatorm_pbuffer-member"></a>CMemAllocator :: m \_ pBuffer, membre

Pointeur vers le bloc de mémoire qui contient les mémoires tampons.

## <a name="syntax"></a>Syntaxe


```C++
LPBYTE m_pBuffer;
```



## <a name="remarks"></a>Notes

Les exemples de mémoires tampons sont calculés comme des décalages par rapport à ce pointeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMemAllocator, classe**](cmemallocator.md)
</dt> </dl>

 

 




