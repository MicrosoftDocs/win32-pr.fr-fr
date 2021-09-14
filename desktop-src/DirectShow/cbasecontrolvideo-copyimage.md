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
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999774"
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

## <a name="return-value"></a>Valeur de retour

Si le paramètre *pVideoImage* est **null**, le paramètre *pBufferSize* est renseigné avec le nombre d’octets requis par la mémoire tampon de sortie pour stocker l’image. Si la mémoire tampon transmise est trop petite ou si la fonction membre ne parvient pas à allouer suffisamment de mémoire, la fonction membre retourne E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

La fonction membre récupère l’image à partir de l’exemple et la copie dans la mémoire tampon de sortie. La section de la vidéo copiée dans la mémoire tampon de sortie reflète le rectangle source qui est défini par l’interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) (bien qu’elle ne reflète pas le rectangle de destination).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




