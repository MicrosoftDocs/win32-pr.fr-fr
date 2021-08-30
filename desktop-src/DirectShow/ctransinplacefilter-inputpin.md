---
description: La méthode InputPin récupère un pointeur vers la broche d’entrée du filtre.
ms.assetid: 533a962e-225d-4f10-a9c3-1464bea512ba
title: Méthode CTransInPlaceFilter. InputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.InputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e70e91780ba1c0d1e1a3d204a6d99826e80a2fe23cbac4125d0b6300e4fdf005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083889"
---
# <a name="ctransinplacefilterinputpin-method"></a>Méthode CTransInPlaceFilter. InputPin

La `InputPin` méthode récupère un pointeur vers la broche d’entrée du filtre.

## <a name="syntax"></a>Syntaxe


```C++
CTransInPlaceInputPin* InputPin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la variable de membre [**CTransformFilter :: m \_ pInput**](ctransformfilter-m-pinput.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




