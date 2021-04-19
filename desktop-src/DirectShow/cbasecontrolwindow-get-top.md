---
description: La \_ méthode obtenir le haut récupère la coordonnée de fenêtre supérieure.
ms.assetid: 1e7910bd-e38e-4586-9dd6-701f69c0f6e7
title: Méthode CBaseControlWindow.get_Top (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9861d930cdb2d93e5e0b73ffad625885c082cb6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537862"
---
# <a name="cbasecontrolwindowget_top-method"></a>CBaseControlWindow. obtient la \_ méthode Top

La `get_Top` méthode récupère la coordonnée de fenêtre supérieure.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Top(
   long *pTop
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTop* 
</dt> <dd>

Pointeur vers la coordonnée supérieure, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

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

 

 




