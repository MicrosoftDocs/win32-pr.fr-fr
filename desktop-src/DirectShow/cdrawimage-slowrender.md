---
description: La méthode SlowRender dessine l’image vidéo à l’aide des fonctions SetDIBitsToDevice ou StretchDIBits.
ms.assetid: e1d8b189-b588-48eb-988a-3e5dedb38dbd
title: Méthode CDrawImage. SlowRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SlowRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b736bf6c44d4ada6e0a28408c449c9f8b2f1e1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528092"
---
# <a name="cdrawimageslowrender-method"></a>Méthode CDrawImage. SlowRender

La `SlowRender` méthode dessine l’image vidéo à l’aide des fonctions **SetDIBitsToDevice** ou **StretchDIBits** .

## <a name="syntax"></a>Syntaxe


```C++
void SlowRender(
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

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si [**CDrawImage :: UsingImageAllocator**](cdrawimage-usingimageallocator.md) retourne **false**, la méthode [**CDrawImage ::D rawimage**](cdrawimage-drawimage.md) utilise `SlowRender` pour dessiner l’image vidéo. Dans le cas contraire, DrawImage utilise la méthode **FastRender** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::FastRender**](cdrawimage-fastrender.md)
</dt> </dl>

 

 




