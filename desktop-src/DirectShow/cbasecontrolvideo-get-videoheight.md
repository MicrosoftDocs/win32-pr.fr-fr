---
description: La \_ méthode obtenir VideoHeight récupère la hauteur de la vidéo native.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: Méthode CBaseControlVideo.get_VideoHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31a7ca4b87a9196a8b59ec00cdc0e458855fa1db4e1e8f7b5bfd233924475519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057079"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a>Méthode CBaseControlVideo. obten \_ VideoHeight

La `get_VideoHeight` méthode récupère la hauteur de la vidéo native.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVideoHeight* 
</dt> <dd>

Pointeur vers la hauteur de la vidéo native, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une erreur erronée en cas de réussite ou E \_ OUTOFMEMORY si la mémoire disponible est insuffisante.

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) . Elle appelle la CBaseControlVideo virtuelle pure [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) pour récupérer la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à partir de la classe dérivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




