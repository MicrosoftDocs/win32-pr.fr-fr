---
description: 'La méthode CurrentRate récupère la vitesse du segment, définie par la méthode CBasePin :: NewSegment.'
ms.assetid: 19780dd2-2dcf-4e5d-8a70-a46be05e040c
title: Méthode CBasePin. CurrentRate (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: adffcc02aad4c5516a8e92c247e47b7dbf389d73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999348"
---
# <a name="cbasepincurrentrate-method"></a>Méthode CBasePin. CurrentRate

La `CurrentRate` méthode récupère la vitesse du segment, définie par la méthode [**CBasePin :: NewSegment**](cbasepin-newsegment.md) .

## <a name="syntax"></a>Syntaxe


```C++
double CurrentRate();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne la valeur de [**CBasePin :: m \_ dRate**](cbasepin-m-drate.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




