---
description: La méthode OnStartStreaming réinitialise toutes les fois qui contrôlent la diffusion en continu.
ms.assetid: a2bb07f2-6880-4030-96c5-d146982dfe66
title: Méthode CBaseVideoRenderer. OnStartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403d465d4ff9fe8ae9101b13e2ec5e6c04bdddf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540947"
---
# <a name="cbasevideorendereronstartstreaming-method"></a>Méthode CBaseVideoRenderer. OnStartStreaming

La `OnStartStreaming` méthode réinitialise toutes les fois qui contrôlent la diffusion en continu.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnStartStreaming();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre substitue [**CBaseRenderer :: OnStartStreaming**](cbaserenderer-onstartstreaming.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




