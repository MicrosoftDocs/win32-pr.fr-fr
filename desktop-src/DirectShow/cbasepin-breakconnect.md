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
ms.openlocfilehash: a9a099b1001c2b8c30398ca350e05d15562a8bc2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099437"
---
# <a name="cbasepinbreakconnect-method"></a>Méthode CBasePin. BreakConnect

La `BreakConnect` méthode libère le code confidentiel d’une connexion.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

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

 

 




