---
description: La méthode obtenir le \_ débit binaire récupère une vitesse de transmission approximative pour la vidéo.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: Méthode CBaseControlVideo.get_BitRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f1feaed786b397801bbd17d2d2d41c0ccb813d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296847"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a>CBaseControlVideo. obtient la \_ méthode de débit binaire

La `get_BitRate` méthode récupère une vitesse de transmission approximative de la vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBitRate* 
</dt> <dd>

Pointeur vers la vitesse de transmission, en bits par seconde.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une erreur en cas de réussite ou E \_ OUTOFMEMORY si la mémoire disponible est insuffisante.

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IBasicVideo :: obtient le \_ débit binaire**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) . Elle appelle la CBaseControlVideo virtuelle pure [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) pour récupérer la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à partir de la classe dérivée.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




