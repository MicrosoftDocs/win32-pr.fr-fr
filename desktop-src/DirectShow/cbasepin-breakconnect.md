---
description: La méthode BreakConnect libère le code confidentiel d’une connexion.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Méthode CBasePin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8964ea76e48e4753f42923663ab45962cd672e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526661"
---
# <a name="cbasepinbreakconnect-method"></a>Méthode CBasePin. BreakConnect

La `BreakConnect` méthode libère le code confidentiel d’une connexion.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode est appelée lors de la déconnexion du code confidentiel par la méthode [**CBasePin ::D éconnecter**](cbasepin-disconnect.md) . Elle est également appelée pendant une tentative de connexion si la méthode [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) échoue.

Cette méthode doit libérer toutes les ressources qui ont été obtenues par la méthode **CheckConnect** . Par exemple, si **CheckConnect** alloue de la mémoire, `BreakConnect` doit libérer de la mémoire. Si **CheckConnect** interroge le code PIN de connexion pour une interface, `BreakConnect` doit libérer l’interface.

Notez que `BreakConnect` peut être appelé sans appel correspondant à **CompleteConnect**. Par conséquent, vous ne pouvez pas supposer que **CompleteConnect** a été appelé précédemment.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




