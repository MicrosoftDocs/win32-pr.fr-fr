---
description: La méthode SetStretchMode calcule si l’image vidéo doit être étirée.
ms.assetid: ffdcaf9c-e157-4557-9193-8430c1c451bf
title: Méthode CDrawImage. SetStretchMode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetStretchMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3886910bce57aca728f64ffbe9d660c1073d1281864a7721faa7e757c7c7d81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526489"
---
# <a name="cdrawimagesetstretchmode-method"></a>Méthode CDrawImage. SetStretchMode

La `SetStretchMode` méthode calcule si l’image vidéo doit être étirée.

## <a name="syntax"></a>Syntaxe


```C++
void SetStretchMode();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La classe **CDrawImage** appelle automatiquement cette méthode chaque fois que le rectangle source ou cible change.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CDrawImage, classe**](cdrawimage.md)
</dt> </dl>

 

 




