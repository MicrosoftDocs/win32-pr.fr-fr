---
description: La méthode OnStopStreaming est appelée à la fin de streaming pour corriger les temps pour le rapport de page de propriétés.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Méthode CBaseVideoRenderer. OnStopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38e1e3fef83bab4d598cfd36294c5c405c1eca938372b43f12a6401c4be3c46b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586039"
---
# <a name="cbasevideorendereronstopstreaming-method"></a>Méthode CBaseVideoRenderer. OnStopStreaming

La `OnStopStreaming` méthode est appelée à la fin de streaming pour corriger les durées du rapport de page de propriétés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette fonction membre est appelée deux fois, une fois lors de la suspension et de nouveau lorsque le flux est effectivement arrêté.

Cette fonction membre substitue [**CBaseRenderer :: OnStopStreaming**](cbaserenderer-onstopstreaming.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




