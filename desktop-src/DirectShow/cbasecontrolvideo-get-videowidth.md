---
description: La \_ méthode obtenir VideoWidth récupère la largeur de la vidéo native.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: Méthode CBaseControlVideo.get_VideoWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: faeeed7ea8af58103e74d9b8c3690523c893282f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533500"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a>Méthode CBaseControlVideo. obten \_ VideoWidth

La `get_VideoWidth` méthode récupère la largeur de la vidéo native.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVideoWidth* 
</dt> <dd>

Pointeur vers la largeur de la vidéo native, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une erreur erronée en cas de réussite ou E \_ OUTOFMEMORY si la mémoire disponible est insuffisante.

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) . Elle appelle la CBaseControlVideo virtuelle pure [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) pour récupérer la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à partir de la classe dérivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




