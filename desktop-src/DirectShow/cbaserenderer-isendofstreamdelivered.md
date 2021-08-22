---
description: La méthode IsEndOfStreamDelivered demande si l' \_ événement EC Complete a été remis au gestionnaire du graphique de filtres.
ms.assetid: 13138626-35b0-4da1-9c7e-5d22d86ad2e3
title: Méthode CBaseRenderer. IsEndOfStreamDelivered (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStreamDelivered
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f15c2bca14e6c0f55f46441bbb4de362e6375d0b67f3012a4ad234a9366b188
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954878"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a>Méthode CBaseRenderer. IsEndOfStreamDelivered

La `IsEndOfStreamDelivered` méthode détermine si l' \_ événement EC Complete a été remis au gestionnaire du graphique de filtres.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’indicateur [**CBaseRenderer :: m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




