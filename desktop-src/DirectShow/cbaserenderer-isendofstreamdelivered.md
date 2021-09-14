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
ms.openlocfilehash: f60216afc6481411010fb2f2b0618c36a7d7acf4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111298"
---
# <a name="cbaserendererisendofstreamdelivered-method"></a>Méthode CBaseRenderer. IsEndOfStreamDelivered

La `IsEndOfStreamDelivered` méthode détermine si l' \_ événement EC Complete a été remis au gestionnaire du graphique de filtres.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsEndOfStreamDelivered();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne l’indicateur [**CBaseRenderer :: m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




