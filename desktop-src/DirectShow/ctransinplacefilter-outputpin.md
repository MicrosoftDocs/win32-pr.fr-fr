---
description: La méthode OutputPin récupère un pointeur vers la broche de sortie du filtre.
ms.assetid: 8c8c125e-553d-43c5-bc63-a0c7d5b01260
title: Méthode CTransInPlaceFilter. OutputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.OutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cccd1f6c47488f1330e97a3e5b95b1dbea3a3b5c43b6395dfe6246214109bdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907269"
---
# <a name="ctransinplacefilteroutputpin-method"></a>Méthode CTransInPlaceFilter. OutputPin

La `OutputPin` méthode récupère un pointeur vers la broche de sortie du filtre.

## <a name="syntax"></a>Syntaxe


```C++
CTransInPlaceOutputPin* OutputPin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la variable de membre [**CTransformFilter :: m \_ pOutput**](ctransformfilter-m-poutput.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




