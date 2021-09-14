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
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123741"
---
# <a name="cbasevideorendereronstopstreaming-method"></a>Méthode CBaseVideoRenderer. OnStopStreaming

La `OnStopStreaming` méthode est appelée à la fin de streaming pour corriger les durées du rapport de page de propriétés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre est appelée deux fois, une fois lors de la suspension et de nouveau lorsque le flux est effectivement arrêté.

Cette fonction membre substitue [**CBaseRenderer :: OnStopStreaming**](cbaserenderer-onstopstreaming.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




