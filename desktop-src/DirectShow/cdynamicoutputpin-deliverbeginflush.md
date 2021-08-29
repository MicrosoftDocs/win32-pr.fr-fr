---
description: 'Méthode CDynamicOutputPin. DeliverBeginFlush : la méthode DeliverBeginFlush demande à la broche d’entrée connectée de commencer une opération de vidage.'
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: Méthode CDynamicOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06b7486fa8fbacb4f2d048da198a78aa763e9beabc1991b2ddd178b9a55781b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055939"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a>Méthode CDynamicOutputPin. DeliverBeginFlush

La `DeliverBeginFlush` méthode demande à la broche d’entrée connectée de commencer une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.

## <a name="remarks"></a>Remarques

Cette méthode remplace la méthode [**CBaseOutputPin ::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) . Il définit l’événement [**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




