---
description: La méthode CopyPalette copie la palette de toute structure VIDEOINFO vers n’importe quelle structure VIDEOINFO en palette.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Méthode CImagePalette. CopyPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542733"
---
# <a name="cimagepalettecopypalette-method"></a>Méthode CImagePalette. CopyPalette

La `CopyPalette` méthode copie la palette de toute structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) vers toute structure en palette **VIDEOINFO** .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrc* 
</dt> <dd>

Pointeur vers le type de média source.

</dd> <dt>

*pDest* 
</dt> <dd>

Pointeur vers le type de média de destination.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si la palette a été copiée. Retourne \_ la valeur S false si le type de média source ou de destination n’a pas de palette.

## <a name="remarks"></a>Notes

Le type de média *pDEST* doit être un format en palette avec une profondeur de couleur de 8 bits ou moins. Le type de média *pSrc* peut être n’importe quel type de [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) avec une palette, y compris les formats YUV et couleurs vraies avec des entrées de palette. La méthode copie les entrées de palette de *pSrc* dans une nouvelle palette, puis attache la nouvelle palette à *pDEST*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImagePalette, classe**](cimagepalette.md)
</dt> </dl>

 

 




