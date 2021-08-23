---
description: Méthode constructeur CImagePalette. CImagePalette.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Constructeur CImagePalette. CImagePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 437055ee9e1d33d4b551faf1ca999d432a99d17919dcd67f6a701bc4f9780543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428919"
---
# <a name="cimagepalettecimagepalette-constructor"></a>Constructeur CImagePalette. CImagePalette

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pBaseFilter* 
</dt> <dd>

Pointeur vers le filtre propriétaire.

</dd> <dt>

*pBaseWindow* 
</dt> <dd>

Pointeur vers un objet **CBaseWindow** , qui gère la fenêtre dans laquelle la palette est réalisée. Ce paramètre peut être **NULL**.

</dd> <dt>

*pDrawImage* 
</dt> <dd>

Pointeur vers un objet **CDrawImage** , qui dessine l’image vidéo. Ce paramètre peut être **NULL**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CImagePalette, classe**](cimagepalette.md)
</dt> </dl>

 

 




