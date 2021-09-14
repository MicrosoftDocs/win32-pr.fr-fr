---
description: 'Méthode CDynamicOutputPin. DeliverEndFlush : la méthode DeliverEndFlush demande à la broche d’entrée connectée de terminer une opération de vidage.'
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Méthode CDynamicOutputPin. DeliverEndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b6952ff50dc2266655c58bd5c2e1ed13105598
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999722"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a>Méthode CDynamicOutputPin. DeliverEndFlush

La `DeliverEndFlush` méthode demande à la broche d’entrée connectée de terminer une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.

## <a name="remarks"></a>Notes

Cette méthode remplace la méthode [**CBaseOutputPin ::D eliverendflush**](cbaseoutputpin-deliverendflush.md) . Il réinitialise l’événement [**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




