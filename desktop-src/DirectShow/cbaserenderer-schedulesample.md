---
description: La méthode ScheduleSample planifie un exemple de rendu.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Méthode CBaseRenderer. ScheduleSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88e728b90078ab11a6215dad60a88b819b2c513071637e2aa5c6b6ed7226189b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157591"
---
# <a name="cbaserendererschedulesample-method"></a>Méthode CBaseRenderer. ScheduleSample

La `ScheduleSample` méthode planifie un exemple de rendu.

## <a name="syntax"></a>Syntaxe


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si l’exemple a été planifié, ou **false** si l’exemple a été supprimé.

## <a name="remarks"></a>Remarques

Cette méthode détermine d’abord si l’exemple doit être rendu immédiatement, rendu dans le futur ou supprimé. (Pour ce faire, elle appelle la méthode [**CBaseRenderer :: GetSampleTimes**](cbaserenderer-getsampletimes.md) .) Si l’exemple doit être rendu immédiatement, la méthode signale l’événement [**CBaseRenderer :: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) . Si l’exemple doit être rendu à l’avenir, la méthode appelle la méthode [**IReferenceClock :: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) pour la planification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




