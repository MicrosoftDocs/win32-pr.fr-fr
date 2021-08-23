---
description: 'Méthode CMemAllocator. Alloc : la méthode Alloc alloue de la mémoire pour les mémoires tampons.'
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: CMemAllocator. Alloc, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93d3f367b0aa69fd2b5782e7cf3c830c30f140389d8611caadc7b70372762625
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813789"
---
# <a name="cmemallocatoralloc-method"></a>CMemAllocator. Alloc, méthode

La `Alloc` méthode alloue de la mémoire pour les mémoires tampons.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                       | Description                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Réussite.<br/>                          |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>     | Mémoire insuffisante.<br/>              |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | Les exigences de mémoire tampon n’ont pas été définies.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode est appelée par la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) . Elle alloue un bloc de mémoire contigu suffisant pour les exigences de mémoire tampon fournies dans la méthode [**CMemAllocator :: SetProperties**](cmemallocator-setproperties.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMemAllocator, classe**](cmemallocator.md)
</dt> </dl>

 

 




