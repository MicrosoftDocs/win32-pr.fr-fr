---
description: La \_ méthode obtenir AvgTimePerFrame récupère le temps moyen par frame.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: Méthode CBaseControlVideo.get_AvgTimePerFrame (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f80a9b39bf18d92499687e38bac31f3b1105892506b61a5a685d938a60e382cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057309"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a>Méthode CBaseControlVideo. obten \_ AvgTimePerFrame

La `get_AvgTimePerFrame` méthode récupère le temps moyen par frame.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAvgTimePerFrame* 
</dt> <dd>

Pointeur vers le temps moyen par frame.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une erreur erronée en cas de réussite ou E \_ OUTOFMEMORY si la mémoire disponible est insuffisante.

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) . Elle appelle la fonction membre pure [**CBaseControlVideo :: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) pour récupérer la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à partir de la classe dérivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




