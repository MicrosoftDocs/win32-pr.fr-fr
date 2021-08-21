---
description: La méthode WaitForRenderTime attend l’heure de présentation de l’exemple actuel.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Méthode CBaseRenderer. WaitForRenderTime (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e590a09c2c6d4cc34728f5ec29db0d8f650d3a1e9cb663e5993acd2cebe4793f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157353"
---
# <a name="cbaserendererwaitforrendertime-method"></a>Méthode CBaseRenderer. WaitForRenderTime

La `WaitForRenderTime` méthode attend l’heure de présentation de l’exemple actuel.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                           | Description                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Réussite.<br/>                                                       |
| <dl> <dt>**\_État VFW \_ E \_ modifié**</dt> </dl> | L’état du filtre a changé avant l’heure de la présentation.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode attend jusqu’à ce que l’un des éléments suivants se produise :

-   L’heure de présentation de l’exemple arrive, point où l’exemple peut être rendu.
-   Le filtre s’arrête ou commence à vider les données.

Si l’heure de présentation arrive, l’événement [**CBaseRenderer :: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) est signalé. Si l’état change, l’événement [**CBaseRenderer :: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md) est signalé. Cette méthode attend les deux événements. La classe dérivée peut substituer cette méthode pour attendre des événements supplémentaires, si nécessaire.

Cette méthode appelle la méthode [**CBaseRenderer :: OnWaitStart**](cbaserenderer-onwaitstart.md) lorsque l’attente commence, et la méthode [**CBaseRenderer :: OnWaitEnd**](cbaserenderer-onwaitend.md) quand l’attente est terminée. Aucune de ces méthodes ne fait quoi que ce soit dans la classe de base, mais la classe dérivée peut les substituer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




