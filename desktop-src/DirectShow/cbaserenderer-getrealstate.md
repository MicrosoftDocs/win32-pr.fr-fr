---
description: La méthode GetRealState récupère l’état du filtre.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Méthode CBaseRenderer. GetRealState (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541320"
---
# <a name="cbaserenderergetrealstate-method"></a>Méthode CBaseRenderer. GetRealState

La `GetRealState` méthode récupère l’état du filtre.

## <a name="syntax"></a>Syntaxe


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la valeur de l' [**\_ État CBaseFilter :: m**](cbasefilter-m-state.md). La valeur est un membre du type énuméré d' [**\_ État de filtre**](/windows/win32/api/strmif/ne-strmif-filter_state) .

## <a name="remarks"></a>Notes

Cette méthode offre une alternative plus simple à la méthode [**CBaseRenderer :: GetState**](cbaserenderer-getstate.md) , à des fins d’utilisation interne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




