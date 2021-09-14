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
ms.openlocfilehash: 417a18ca53240dce0e4ed6d40f551c45c24b0f1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230406"
---
# <a name="cbaserendereronstopstreaming-method"></a>Méthode CBaseRenderer. OnStopStreaming

La `OnStopStreaming` méthode est appelée lorsque le filtre arrête la diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK.

## <a name="remarks"></a>Notes

La méthode [**CBaseRenderer :: StopStreaming**](cbaserenderer-stopstreaming.md) appelle cette méthode. Elle ne fait rien dans la classe de base, mais la classe dérivée peut la substituer.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




