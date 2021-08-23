---
description: 'La méthode IsPreroll détermine si cet exemple est un exemple de préroll. Un exemple de préroll ne doit pas être affiché. Cette méthode implémente la méthode IMediaSample :: IsPreroll.'
ms.assetid: fbcf7aab-473c-49c1-9a8f-4a619f4e28f4
title: Méthode CMediaSample. IsPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.IsPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f4c4b192d72c5edcfdb9c318f7420ca6ae5797446ec4f99cb6871aad2abd241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634639"
---
# <a name="cmediasampleispreroll-method"></a>Méthode CMediaSample. IsPreroll

La `IsPreroll` méthode détermine si cet exemple est un exemple de préroll. Un exemple de préroll ne doit pas être affiché. Cette méthode implémente la méthode [**IMediaSample :: IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si l’exemple est un exemple de préroll et s \_ false dans le cas contraire.

## <a name="remarks"></a>Remarques

La variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) spécifie cette propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




