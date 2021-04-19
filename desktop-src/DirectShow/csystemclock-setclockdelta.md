---
description: 'La méthode SetClockDelta ajuste l’heure de l’horloge. Cette méthode implémente la méthode IAMClockAdjust :: SetClockDelta.'
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Méthode CSystemClock. SetClockDelta (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530373"
---
# <a name="csystemclocksetclockdelta-method"></a>Méthode CSystemClock. SetClockDelta

La `SetClockDelta` méthode ajuste l’heure de l’horloge. Cette méthode implémente la méthode [**IAMClockAdjust :: SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rtDelta* 
</dt> <dd>

Spécifie la quantité d’ajustement de l’horloge, en tant que valeur de [**\_ temps de référence**](reference-time.md) . Une valeur positive déplace l’avance de l’horloge et une valeur négative déplace l’horloge vers l’arrière.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne \_ un ou un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode appelle simplement [**CBaseReferenceClock :: SetTimeDelta**](cbasereferenceclock-settimedelta.md).

Les valeurs d’heure retournées par [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) augmentent de manière monotone. Si vous redéfinissez l’horloge, **getTime** continue à signaler l’ancienne fois jusqu’à ce que l’horloge interne rattrape.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | CSystemClock, classe<br/>                                                                                                                                                              |
| En-tête<br/>  | <dl> <dt>Sysclock. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




