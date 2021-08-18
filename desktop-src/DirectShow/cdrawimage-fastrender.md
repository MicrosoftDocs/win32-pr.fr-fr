---
description: La méthode FastRender dessine l’image vidéo à l’aide des fonctions BitBlt ou StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Méthode CDrawImage. FastRender (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146c3736f7aaa89fc9a724d9dd7e4bfb58160e21e2de57f40a8e855c8a3c1446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043602"
---
# <a name="cdrawimagefastrender-method"></a>Méthode CDrawImage. FastRender

La `FastRender` méthode dessine l’image vidéo à l’aide des fonctions **BitBlt** ou **StretchBlt** .

## <a name="syntax"></a>Syntaxe


```C++
void FastRender(
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

## <a name="remarks"></a>Remarques

La méthode [**CDrawImage ::D rawimage**](cdrawimage-drawimage.md) appelle cette méthode, mais uniquement si l’allocateur pour la connexion est un objet [**CImageAllocator**](cimageallocator.md) . Dans ce cas, l’exemple de support est garanti comme un objet [**CImageSample**](cimagesample.md) . L’objet **CImageSample** utilise la fonction **CreateDIBSection** pour allouer de la mémoire partagée pour la bitmap, ce qui permet de dessiner l’image à l’aide de **BitBlt** ou de **StretchBlt**.

Cette méthode appelle **BitBlt** si les rectangles source et cible correspondent exactement, ou **StretchBlt** dans le cas contraire.

Si le filtre n’est pas propriétaire de l’allocateur, la méthode **DrawImage** utilise [**CDrawImage :: SlowRender**](cdrawimage-slowrender.md) pour dessiner l’image.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




