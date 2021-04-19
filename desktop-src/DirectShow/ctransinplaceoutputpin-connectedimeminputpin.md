---
description: 'La méthode ConnectedIMemInputPin récupère un pointeur vers la broche d’entrée en aval. Cette méthode retourne la variable de membre CBaseOutputPin :: m \_ pInputPin.'
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Méthode CTransInPlaceOutputPin. ConnectedIMemInputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540224"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a>Méthode CTransInPlaceOutputPin. ConnectedIMemInputPin

La `ConnectedIMemInputPin` méthode récupère un pointeur vers la broche d’entrée en aval. Cette méthode retourne la variable de membre [**CBaseOutputPin :: m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md) .

## <a name="syntax"></a>Syntaxe


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sur la broche d’entrée en aval.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceOutputPin, classe**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




