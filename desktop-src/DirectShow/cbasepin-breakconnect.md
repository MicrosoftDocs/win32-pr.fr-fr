---
description: 'Méthode CBasePin. BreakConnect : la méthode BreakConnect libère le code confidentiel d’une connexion.'
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
ms.openlocfilehash: c40c7614f94b2be5e5f588a706b4b0bd1eec92c3181ffbedcad3ae1e57183f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955228"
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

## <a name="remarks"></a>Remarques

Cette méthode est appelée lors de la déconnexion du code confidentiel par la méthode [**CBasePin ::D éconnecter**](cbasepin-disconnect.md) . Elle est également appelée pendant une tentative de connexion si la méthode [**CBasePin :: CheckConnect**](cbasepin-checkconnect.md) échoue.

Cette méthode doit libérer toutes les ressources qui ont été obtenues par la méthode **CheckConnect** . Par exemple, si **CheckConnect** alloue de la mémoire, `BreakConnect` doit libérer de la mémoire. Si **CheckConnect** interroge le code PIN de connexion pour une interface, `BreakConnect` doit libérer l’interface.

Notez que `BreakConnect` peut être appelé sans appel correspondant à **CompleteConnect**. Par conséquent, vous ne pouvez pas supposer que **CompleteConnect** a été appelé précédemment.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




