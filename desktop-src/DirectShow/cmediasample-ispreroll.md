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
ms.openlocfilehash: b40cf8fd6a1adb5186309f47da0f0ae3dc30412a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223449"
---
# <a name="cmediasampleispreroll-method"></a>Méthode CMediaSample. IsPreroll

La `IsPreroll` méthode détermine si cet exemple est un exemple de préroll. Un exemple de préroll ne doit pas être affiché. Cette méthode implémente la méthode [**IMediaSample :: IsPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-ispreroll) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsPreroll();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK si l’exemple est un exemple de préroll et s \_ false dans le cas contraire.

## <a name="remarks"></a>Notes

La variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) spécifie cette propriété.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




