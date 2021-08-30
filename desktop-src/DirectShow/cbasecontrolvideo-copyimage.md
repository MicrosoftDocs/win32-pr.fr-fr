---
description: Crée une copie de mémoire d’une image.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Méthode CBaseControlVideo. CopyImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20e427a9c8b146dc1398443df06cbb8a3fb58452e3bbabd0a6291428f960a79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057329"
---
# <a name="cbasecontrolvideocopyimage-method"></a>Méthode CBaseControlVideo. CopyImage

Crée une copie de mémoire d’une image.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’exemple contenant l’image vidéo.

</dd> <dt>

*pVideoInfo* 
</dt> <dd>

Pointeur vers le format représentant l’image vidéo.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Pointeur vers la taille de la mémoire tampon de sortie.

</dd> <dt>

*pVideoImage* 
</dt> <dd>

Pointeur vers la mémoire tampon de sortie.

</dd> <dt>

*pSourceRect* 
</dt> <dd>

Pointeur vers le rectangle de la vidéo source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le paramètre *pVideoImage* est **null**, le paramètre *pBufferSize* est renseigné avec le nombre d’octets requis par la mémoire tampon de sortie pour stocker l’image. Si la mémoire tampon transmise est trop petite ou si la fonction membre ne parvient pas à allouer suffisamment de mémoire, la fonction membre retourne E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

La fonction membre récupère l’image à partir de l’exemple et la copie dans la mémoire tampon de sortie. La section de la vidéo copiée dans la mémoire tampon de sortie reflète le rectangle source qui est défini par l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) (bien qu’elle ne reflète pas le rectangle de destination).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




