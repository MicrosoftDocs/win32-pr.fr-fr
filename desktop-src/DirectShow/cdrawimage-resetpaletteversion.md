---
description: La méthode ResetPaletteVersion réinitialise la version de la palette. Appelez cette méthode si le code confidentiel du filtre propriétaire se reconnecte.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: Méthode CDrawImage. ResetPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d367060c86c54fb9df5bd7b0f05cea1fa3d7b7f3316dce327fca7ce9985fadfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055959"
---
# <a name="cdrawimageresetpaletteversion-method"></a>Méthode CDrawImage. ResetPaletteVersion

La `ResetPaletteVersion` méthode réinitialise la version de la palette. Appelez cette méthode si le code confidentiel du filtre propriétaire se reconnecte.

## <a name="syntax"></a>Syntaxe


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode définit la valeur de **m \_ PaletteVersion** sur une constante prédéfinie, **\_ version** de la palette.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> <dt>

[**CDrawImage::GetPaletteVersion**](cdrawimage-getpaletteversion.md)
</dt> <dt>

[**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




