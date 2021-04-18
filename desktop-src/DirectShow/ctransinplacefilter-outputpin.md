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
ms.openlocfilehash: d4e74708062d66c8678af9541df762103ae36537
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532869"
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
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




