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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010009"
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

## <a name="return-value"></a>Valeur de retour

Retourne \_ un ou un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode appelle simplement [**CBaseReferenceClock :: SetTimeDelta**](cbasereferenceclock-settimedelta.md).

Les valeurs d’heure retournées par [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) augmentent de manière monotone. Si vous redéfinissez l’horloge, **getTime** continue à signaler l’ancienne fois jusqu’à ce que l’horloge interne rattrape.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | CSystemClock, classe<br/>                                                                                                                                                              |
| En-tête<br/>  | <dl> <dt>Sysclock. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




