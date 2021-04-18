---
description: 'La méthode SetDiscontinuity spécifie si cet exemple représente une rupture dans le flux de données. Cette méthode implémente la méthode IMediaSample :: SetDiscontinuity.'
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Méthode CMediaSample. SetDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532759"
---
# <a name="cmediasamplesetdiscontinuity-method"></a>Méthode CMediaSample. SetDiscontinuity

La `SetDiscontinuity` méthode spécifie si cet exemple représente une rupture dans le flux de données. Cette méthode implémente la méthode [**IMediaSample :: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bDiscont* 
</dt> <dd>

Valeur booléenne qui spécifie si cet exemple est une discontinuité. Si la **valeur est true**, l’exemple de média est discontinu avec l’exemple précédent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode met à jour la variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) , qui spécifie la propriété discontinu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




