---
description: 'La méthode CurrentStartTime récupère l’heure de début du segment, définie par la méthode CBasePin :: NewSegment.'
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: Méthode CBasePin. CurrentStartTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f413419992d66f8de3a28bb7e39368564ce0803
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999346"
---
# <a name="cbasepincurrentstarttime-method"></a>Méthode CBasePin. CurrentStartTime

La `CurrentStartTime` méthode récupère l’heure de début du segment, définie par la méthode [**CBasePin :: NewSegment**](cbasepin-newsegment.md) .

## <a name="syntax"></a>Syntaxe


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la valeur de [**CBasePin :: m \_ tStart**](cbasepin-m-tstart.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




