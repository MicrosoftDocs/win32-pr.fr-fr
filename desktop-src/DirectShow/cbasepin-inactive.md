---
description: 'CBasePin. inactive, méthode : la méthode inactive indique au code confidentiel que le filtre n’est plus actif.'
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: CBasePin. inactive, méthode (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8307f3823758eee2f70368e41d3f2dc01333fd538fe2feed30d31b7db876f118
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052739"
---
# <a name="cbasepininactive-method"></a>CBasePin. inactive, méthode

La `Inactive` méthode notifie le code confidentiel que le filtre n’est plus actif.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Quand le filtre s’arrête, la classe [**CBaseFilter**](cbasefilter.md) appelle cette méthode sur toutes les broches connectées du filtre.

Cette méthode n’a aucun effet dans la classe de base. Les classes dérivées doivent remplacer cette méthode pour libérer toutes les ressources obtenues par la méthode [**CBasePin :: active**](cbasepin-active.md) ; par exemple, pour désallouer les allocateurs du pin.

L’état interne du gestionnaire de graphique de filtre n’est pas mis à jour tant que cette méthode n’a pas retourné de valeur, donc ne Testez pas l’État à partir de cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




