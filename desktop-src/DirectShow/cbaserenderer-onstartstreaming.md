---
description: La méthode OnStartStreaming est appelée quand le filtre commence la diffusion en continu.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Méthode CBaseRenderer. OnStartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b0f050222b0ca6a88c7cf1d9348597e4d7b68f2a2ed431b4f6843afe97efd5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157672"
---
# <a name="cbaserendereronstartstreaming-method"></a>Méthode CBaseRenderer. OnStartStreaming

La `OnStartStreaming` méthode est appelée lorsque le filtre commence la diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

La méthode [**CBaseRenderer :: StartStreaming**](cbaserenderer-startstreaming.md) appelle cette méthode. Elle ne fait rien dans la classe de base, mais la classe dérivée peut la substituer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




