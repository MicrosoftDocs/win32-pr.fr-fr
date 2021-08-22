---
description: La méthode ResetEndOfStreamTimer annule la minuterie qui planifie les \_ notifications complètes ec.
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: Méthode CBaseRenderer. ResetEndOfStreamTimer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStreamTimer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e589288059eabbbbaaa23904ba021199cb051d9034345cb2c92ac946a6cba9c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502679"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a>Méthode CBaseRenderer. ResetEndOfStreamTimer

La `ResetEndOfStreamTimer` méthode annule la minuterie qui planifie les notifications [**\_ complètes EC**](ec-complete.md) .

## <a name="syntax"></a>Syntaxe


```C++
void ResetEndOfStreamTimer();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md)
</dt> <dt>

[**CBaseRenderer :: TimerCallback**](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




