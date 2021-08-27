---
description: La méthode DoRenderSample restitue un exemple.
ms.assetid: cf06192c-44c0-4d88-a20e-6501ea48cbfd
title: Méthode CBaseRenderer. DoRenderSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.DoRenderSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef91e7ad27d008f5dfdb83e5642ecba8ec68bc424824dca9c8aa068ec055f24f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076429"
---
# <a name="cbaserendererdorendersample-method"></a>Méthode CBaseRenderer. DoRenderSample

La `DoRenderSample` méthode restitue un exemple.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT DoRenderSample(
   IMediaSample *pMediaSample
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

La classe dérivée doit implémenter cette méthode. Le comportement dépend entièrement du type de filtre implémenté. Un convertisseur vidéo, par exemple, dessinerait l’image vidéo contenue dans l’exemple.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




