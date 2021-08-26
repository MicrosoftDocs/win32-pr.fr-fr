---
description: La méthode DrawImage dessine une image vidéo dans la fenêtre vidéo.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: CDrawImage. DrawImage, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2791d20b906f2a2adce31ce99b9e7498854c8fca00ade4507db0207e04b2cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043603"
---
# <a name="cdrawimagedrawimage-method"></a>CDrawImage. DrawImage, méthode

La `DrawImage` méthode dessine une image vidéo dans la fenêtre vidéo.

## <a name="syntax"></a>Syntaxe


```C++
BOOL DrawImage(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple qui contient l’image.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette méthode délègue à [**CDrawImage :: FastRender**](cdrawimage-fastrender.md) ou [**CDrawImage :: SlowRender**](cdrawimage-slowrender.md), selon que le filtre possède ou non l’allocateur qui a fourni l’exemple. Si le filtre est propriétaire de l’Allocator, il est garanti que l’exemple est un objet [**CImageSample**](cimagesample.md) . Dans ce cas, l’exemple utilise la mémoire partagée allouée par GDI, et l’image peut être dessinée à l’aide de **BitBlt** ou de **StretchBlt**. Dans le cas contraire, les images doivent être dessinées à l’aide des fonctions **SetDIBitsToDevice** ou **StretchDIBits** plus lentes.

Dans les versions Debug, cette méthode appelle **DisplaySampleTimes** pour dessiner les horodatages de l’exemple sur l’image vidéo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




