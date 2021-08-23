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
ms.openlocfilehash: 4189498c60a52692c057a867dba8bc48c43d2b1c32fbd6091738a3711102f4b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832179"
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

## <a name="remarks"></a>Remarques

Cette méthode met à jour la variable de membre [**CMediaSample :: m \_ dwFlags**](cmediasample-m-dwflags.md) , qui spécifie la propriété discontinu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaSample, classe**](cmediasample.md)
</dt> </dl>

 

 




