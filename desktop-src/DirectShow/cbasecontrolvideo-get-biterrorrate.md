---
description: La \_ méthode obtenir BitErrorRate récupère un taux d’erreur de bit approximatif pour la vidéo.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: Méthode CBaseControlVideo.get_BitErrorRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532846"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a>Méthode CBaseControlVideo. obten \_ BitErrorRate

La `get_BitErrorRate` méthode récupère un taux d’erreur de bit approximatif pour la vidéo.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBitErrorRate* 
</dt> <dd>

Pointeur vers le taux d’erreur binaire (une erreur pour approximativement ce nombre de bits).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une erreur erronée en cas de réussite ou E \_ OUTOFMEMORY si la mémoire disponible est insuffisante.

## <a name="remarks"></a>Notes

Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) . Elle appelle la méthode [**CBaseControlVideo :: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtuelle pure pour récupérer la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à partir de la classe dérivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




