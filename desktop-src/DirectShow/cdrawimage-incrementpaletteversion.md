---
description: La méthode IncrementPaletteVersion incrémente la version de la palette. Appelez cette méthode si le type de média passe à un nouveau format en palette.
ms.assetid: 1ce77f97-d225-45f5-a259-1dcca1272d15
title: Méthode CDrawImage. IncrementPaletteVersion (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.IncrementPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21b4220ec98c5b083913e92f5749866f629a4854
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999268"
---
# <a name="cdrawimageincrementpaletteversion-method"></a>Méthode CDrawImage. IncrementPaletteVersion

La `IncrementPaletteVersion` méthode incrémente la version de la palette. Appelez cette méthode si le type de média passe à un nouveau format en palette.

## <a name="syntax"></a>Syntaxe


```C++
void IncrementPaletteVersion();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode incrémente la valeur de la variable membre **m \_ PaletteVersion** .

## <a name="requirements"></a>Spécifications



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

[**CDrawImage::ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




