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
ms.openlocfilehash: 66433795b0674e1d2d5b7a7de5b1dcd1b50eb424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542576"
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

## <a name="remarks"></a>Notes

La méthode [**CBaseRenderer :: StartStreaming**](cbaserenderer-startstreaming.md) appelle cette méthode. Elle ne fait rien dans la classe de base, mais la classe dérivée peut la substituer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




