---
description: La méthode active est appelée lorsque l’état passe à suspendu ou en cours d’exécution.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: CBaseRenderer. active, méthode (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df5ec659b5e76940ebf279e3feb8995d34380db0543d9eebcf42c1f3bff8c0e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954968"
---
# <a name="cbaserendereractive-method"></a>CBaseRenderer. active, méthode

La `Active` méthode est appelée lorsque l’état passe à suspendu ou en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

La broche d’entrée appelle cette méthode à partir de sa propre méthode [**CRendererInputPin :: active**](crendererinputpin-active.md) . Cette méthode n’a aucun effet dans la classe de base.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




