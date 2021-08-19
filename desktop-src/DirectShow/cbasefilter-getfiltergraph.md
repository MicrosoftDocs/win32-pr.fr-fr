---
description: La méthode GetFilterGraph récupère un pointeur vers le gestionnaire de graphique de filtre.
ms.assetid: 80b41272-2ca1-40db-8624-0d99d66f3c34
title: Méthode CBaseFilter. GetFilterGraph (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f35b40febff058d5bbd9f48c5ac6d10168d48d6e587b51ab2730704724e48c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056649"
---
# <a name="cbasefiltergetfiltergraph-method"></a>Méthode CBaseFilter. GetFilterGraph

La `GetFilterGraph` méthode récupère un pointeur vers le gestionnaire de graphique de filtre.

## <a name="syntax"></a>Syntaxe


```C++
IFilterGraph* GetFilterGraph();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la valeur de [**CBaseFilter :: m \_ pGraph**](cbasefilter-m-pgraph.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




