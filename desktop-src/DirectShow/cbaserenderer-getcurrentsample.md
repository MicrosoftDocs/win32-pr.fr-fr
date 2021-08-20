---
description: La méthode GetCurrentSample récupère l’exemple actuel.
ms.assetid: cfdc66e3-7d32-47b7-87f6-99dd9513c93b
title: Méthode CBaseRenderer. GetCurrentSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetCurrentSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ffe3cdf95d5ab248956e670c04572140fa4621fff5b0cb5183f9a7cbd9b837e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822720"
---
# <a name="cbaserenderergetcurrentsample-method"></a>Méthode CBaseRenderer. GetCurrentSample

La `GetCurrentSample` méthode récupère l’exemple actuel.

## <a name="syntax"></a>Syntaxe


```C++
virtual IMediaSample* GetCurrentSample();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple, ou **null** si aucun échantillon n’est disponible.

## <a name="remarks"></a>Remarques

À moins que la méthode ne retourne la **valeur null**, la méthode appelle **AddRef** sur le pointeur [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) avant de la retourner. L’appelant doit libérer le pointeur. (Par implication, vous devez affecter la valeur de retour à une variable, afin de pouvoir la libérer ultérieurement.)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




