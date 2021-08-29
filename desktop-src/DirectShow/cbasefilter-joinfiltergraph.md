---
description: 'La méthode JoinFilterGraph avertit le filtre qu’il a rejoint un graphique de filtre. Cette méthode implémente la méthode IBaseFilter :: JoinFilterGraph.'
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: Méthode CBaseFilter. JoinFilterGraph (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04dc47237ee7bd6f05ba4c187a0d643b478f6e98b74f7670e87df998998dcd03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076629"
---
# <a name="cbasefilterjoinfiltergraph-method"></a>Méthode CBaseFilter. JoinFilterGraph

La `JoinFilterGraph` méthode informe le filtre qu’elle a rejoint un graphique de filtre. Cette méthode implémente la méthode [**IBaseFilter :: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pGraph* 
</dt> <dd>

Pointeur vers l’interface [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) du gestionnaire de graphique de filtre, ou **null** si le filtre quitte le graphique.

</dd> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode contenant un nom pour le filtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Cette méthode définit la variable de membre [**CBaseFilter :: m \_ pGraph**](cbasefilter-m-pgraph.md) comme étant égale au paramètre *pGraph* . Il interroge également un pointeur d’interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) et le stocke dans la variable membre [**CBaseFilter :: m \_ pSink**](cbasefilter-m-psink.md) . Toutefois, le filtre ne conserve pas de nombre de références sur l’une de ces interfaces. Cela créerait un nombre de références circulaires, car le gestionnaire de graphes de filtre conserve un décompte de références sur le filtre.

La méthode copie la chaîne spécifiée par *pname* dans la variable membre [**CBaseFilter :: m \_ pname**](cbasefilter-m-pname.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseFilter, classe**](cbasefilter.md)
</dt> </dl>

 

 




