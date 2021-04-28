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
ms.openlocfilehash: e4158a3d6191325e8b647e4551133952d623f795
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099317"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a>Méthode CDynamicOutputPin. DeliverBeginFlush

La `DeliverBeginFlush` méthode demande à la broche d’entrée connectée de commencer une opération de vidage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.

## <a name="remarks"></a>Notes 

Cette méthode remplace la méthode [**CBaseOutputPin ::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) . Il définit l’événement [**CDynamicOutputPin :: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDynamicOutputPin, classe**](cdynamicoutputpin.md)
</dt> </dl>

 

 




