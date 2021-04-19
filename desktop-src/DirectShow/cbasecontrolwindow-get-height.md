---
description: La méthode d’extraction de la \_ hauteur récupère la hauteur de la fenêtre active.
ms.assetid: 841c7d5d-f633-41fb-9cde-6126cd1cab9b
title: Méthode CBaseControlWindow.get_Height (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bed7beaac064ce9d97b9c93264eab8d56b27c9df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537973"
---
# <a name="cbasecontrolwindowget_height-method"></a>CBaseControlWindow. obtient la \_ méthode Height

La `get_Height` méthode récupère la hauteur de la fenêtre actuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Height(
   long *pHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pHeight* 
</dt> <dd>

Pointeur vers la hauteur de la fenêtre active, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

La fenêtre a une position sur le bureau. Ce pourcentage est exprimé en pixels par quatre coordonnées (gauche, haut, droit et bas). Les interfaces automatisées par OLE expriment généralement cette position à gauche, en haut, à largeur et en hauteur ; Il s’agit de la Convention utilisée dans DirectShow. Toutes les coordonnées sont exprimées en pixels, et la modification de toute coordonnée met immédiatement à jour la fenêtre.

La définition des coordonnées gauche ou supérieure déplace la fenêtre vers la gauche ou vers le haut, respectivement ; ces coordonnées n’ont aucun effet sur la largeur et la hauteur de la fenêtre. De même, la définition de la largeur et de la hauteur n’affecte pas les coordonnées gauche et supérieure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




