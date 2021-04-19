---
description: La méthode SetRealize spécifie si la fenêtre réalise des palettes.
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: Méthode CBaseWindow. SetRealize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541761"
---
# <a name="cbasewindowsetrealize-method"></a>Méthode CBaseWindow. SetRealize

La `SetRealize` méthode spécifie si la fenêtre réalise des palettes.

## <a name="syntax"></a>Syntaxe


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bRealize* 
</dt> <dd>

Valeur booléenne qui spécifie s’il faut réaliser des palettes. Si la **valeur est true**, la méthode [**CBaseWindow :: SetPalette**](cbasewindow-setpalette.md) réalise des palettes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Par défaut, la méthode **SetPalette** réalise la palette spécifiée. Appelez cette méthode pour modifier le comportement par défaut, afin que les palettes soient sélectionnées mais pas réalisées. Cette méthode définit la variable de membre [**CBaseWindow :: m \_ bNoRealize**](cbasewindow-m-bnorealize.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




