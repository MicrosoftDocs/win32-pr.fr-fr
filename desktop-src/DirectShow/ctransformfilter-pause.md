---
description: 'CTransformFilter. pause, méthode : la méthode pause interrompt le filtre. Cette méthode implémente la méthode IMediaFilter ::P ause.'
ms.assetid: 3e3afd14-1c92-4f2b-a367-e10caaeb3b63
title: CTransformFilter. pause, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 51584bc38c49345f6bb1d940aed24a052e9a4f9cd05fc2dc84246a6ba1168fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953498"
---
# <a name="ctransformfilterpause-method"></a>CTransformFilter. pause, méthode

La `Pause` méthode suspend le filtre. Cette méthode implémente la méthode [**IMediaFilter ::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK ou une autre valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode appelle la méthode [**StartStreaming**](ctransformfilter-startstreaming.md) . La méthode **StartStreaming** n’a aucun effet dans la classe de base, mais la classe dérivée peut la substituer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transfrm. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransformFilter, classe**](ctransformfilter.md)
</dt> </dl>

 

 




