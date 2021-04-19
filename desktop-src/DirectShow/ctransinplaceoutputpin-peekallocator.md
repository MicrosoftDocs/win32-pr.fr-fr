---
description: La méthode PeekAllocator retourne un pointeur vers l’allocateur du pin. La méthode n’incrémente pas le nombre de références sur l’interface.
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Méthode CTransInPlaceOutputPin. PeekAllocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805de37e2df2bf5a198107eea69d9107e799598c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523940"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a>Méthode CTransInPlaceOutputPin. PeekAllocator

La `PeekAllocator` méthode retourne un pointeur vers l’allocateur du pin. La méthode n’incrémente pas le nombre de références sur l’interface.

## <a name="syntax"></a>Syntaxe


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la variable de membre [**CBaseOutputPin :: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceOutputPin, classe**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




