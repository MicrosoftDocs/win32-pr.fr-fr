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
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527332"
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

## <a name="remarks"></a>Notes

Cette méthode détermine d’abord si l’exemple doit être rendu immédiatement, rendu dans le futur ou supprimé. (Pour ce faire, elle appelle la méthode [**CBaseRenderer :: GetSampleTimes**](cbaserenderer-getsampletimes.md) .) Si l’exemple doit être rendu immédiatement, la méthode signale l’événement [**CBaseRenderer :: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) . Si l’exemple doit être rendu à l’avenir, la méthode appelle la méthode [**IReferenceClock :: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) pour la planification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseRenderer, classe**](cbaserenderer.md)
</dt> </dl>

 

 




