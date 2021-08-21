---
description: La méthode ScheduleSample remplace la classe de base qui effectue le travail principal pour conserver un nombre d’échantillons dessinés et supprimés (qui sont utilisés par l’implémentation de IQualProp).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Méthode CBaseVideoRenderer. ScheduleSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f68701fd4c4d682d6bcd89c3b82d6bf054188a9bbdcb47c9019b563fad4a877f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658233"
---
# <a name="cbasevideorendererschedulesample-method"></a>Méthode CBaseVideoRenderer. ScheduleSample

La `ScheduleSample` méthode remplace la classe de base qui effectue le travail principal pour conserver un nombre d’échantillons dessinés et supprimés (qui sont utilisés par l’implémentation de [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) ).

## <a name="syntax"></a>Syntaxe


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’exemple de média.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si l’exemple est planifié ; Sinon, retourne **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Renbase. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseVideoRenderer, classe**](cbasevideorenderer.md)
</dt> </dl>

 

 




