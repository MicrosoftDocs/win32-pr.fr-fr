---
description: La méthode GetVideoFormat récupère un exemple de vidéo qui représente le format vidéo actuel.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Méthode CBaseControlVideo. GetVideoFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529983"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a>Méthode CBaseControlVideo. GetVideoFormat

La `GetVideoFormat` méthode récupère un exemple de vidéo qui représente le format vidéo actuel.

## <a name="syntax"></a>Syntaxe


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un pointeur vers une structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) qui contient le format vidéo actuel.

## <a name="remarks"></a>Notes

Pour retourner et vérifier certaines informations par le biais de [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), l’objet doit connaître le format vidéo actuel. Elle obtient ces informations en appelant cette méthode virtuelle pure qui doit être substituée par les classes dérivées. Cette fonction membre est appelée par les fonctions membres [**CBaseControlVideo**](cbasecontrolvideo.md) suivantes.

-   [**CBaseControlVideo::OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)
-   [**CBaseControlVideo :: obtient \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)
-   [**CBaseControlVideo :: obtient la \_ vitesse de transmission**](cbasecontrolvideo-get-bitrate.md)
-   [**CBaseControlVideo :: obtient \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)
-   [**CBaseControlVideo :: obtient \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)
-   [**CBaseControlVideo :: obtient \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)
-   [**CBaseControlVideo::GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)
-   [**CBaseControlVideo::GetVideoSize**](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




