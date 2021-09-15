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
ms.openlocfilehash: 8ae988474196e323cde24305b0e389ac69f0f10d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312465"
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

 

 




