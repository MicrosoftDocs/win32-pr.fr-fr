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
ms.openlocfilehash: 7d7de755aa3b8007a122e43529d16f5e39ca0cb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195627"
---
# <a name="cmemallocatoralloc-method"></a>CMemAllocator. Alloc, méthode

La `Alloc` méthode alloue de la mémoire pour les mémoires tampons.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                                       | Description                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Réussite.<br/>                          |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>     | Mémoire insuffisante.<br/>              |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | Les exigences de mémoire tampon n’ont pas été définies.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode est appelée par la méthode [**CBaseAllocator :: Commit**](cbaseallocator-commit.md) . Elle alloue un bloc de mémoire contigu suffisant pour les exigences de mémoire tampon fournies dans la méthode [**CMemAllocator :: SetProperties**](cmemallocator-setproperties.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMemAllocator, classe**](cmemallocator.md)
</dt> </dl>

 

 




