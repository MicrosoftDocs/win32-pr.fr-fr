---
description: La méthode OnStopStreaming est appelée lorsque le filtre arrête la diffusion en continu.
ms.assetid: d882fec8-09e1-4d36-a09c-44568e743da3
title: Méthode CBaseRenderer. OnStopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5c61490a0719ce45d9776982b9230734d1126cef747330bb595c205500aca331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157662"
---
# <a name="cbaserendereronstopstreaming-method"></a>Méthode CBaseRenderer. OnStopStreaming

La `OnStopStreaming` méthode est appelée lorsque le filtre arrête la diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

La méthode [**CBaseRenderer :: StopStreaming**](cbaserenderer-stopstreaming.md) appelle cette méthode. Elle ne fait rien dans la classe de base, mais la classe dérivée peut la substituer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




