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
ms.openlocfilehash: 2602d203ca5a418dcc889d26932cd28be78d984390e71cff996e6fd3938030a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057289"
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

## <a name="remarks"></a>Remarques

Cette fonction membre implémente la méthode [**IBasicVideo :: obten \_ BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) . Elle appelle la méthode [**CBaseControlVideo :: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) virtuelle pure pour récupérer la structure [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à partir de la classe dérivée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




