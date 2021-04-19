---
description: La méthode Alloc alloue de la mémoire pour les mémoires tampons.
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
ms.openlocfilehash: a142f6c0cea6cdb9b18507becabb909ce67b0fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528720"
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
| <dl> <dt>**\_OK**</dt> </dl>              | Opération réussie.<br/>                          |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>     | Mémoire insuffisante.<br/>              |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | Les exigences de mémoire tampon n’ont pas été définies.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode est appelée par la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) . Elle alloue un bloc de mémoire contigu suffisant pour les exigences de mémoire tampon fournies dans la méthode [**CMemAllocator :: SetProperties**](cmemallocator-setproperties.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMemAllocator, classe**](cmemallocator.md)
</dt> </dl>

 

 




