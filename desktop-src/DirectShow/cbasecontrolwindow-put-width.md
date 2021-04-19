---
description: La \_ méthode put Width définit la largeur de la fenêtre.
ms.assetid: eb5ad1c2-ba39-4c06-84d2-6708dc8796d8
title: Méthode CBaseControlWindow.put_Width (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5235e2b842b26f3f05c31c9f19a16c7630c80c13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541605"
---
# <a name="cbasecontrolwindowput_width-method"></a>CBaseControlWindow. put, \_ méthode de largeur

La `put_Width` méthode définit la largeur de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Width(
   long Width
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Width* 
</dt> <dd>

Nouvelle largeur de la fenêtre, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

La fenêtre a une position sur le bureau. Ce pourcentage est exprimé en pixels par quatre coordonnées (gauche, haut, droit et bas). Les interfaces automatisées par OLE expriment généralement cette position à gauche, en haut, à largeur et en hauteur ; Il s’agit de la Convention utilisée dans DirectShow. Toutes les coordonnées sont exprimées en pixels et la modification de toute coordonnée met immédiatement à jour la fenêtre.

La définition des coordonnées gauche ou supérieure déplace la fenêtre vers la gauche ou vers le haut respectivement ; ces coordonnées n’ont aucun effet sur la largeur et la hauteur de la fenêtre. De même, la définition de la largeur et de la hauteur n’affecte pas les coordonnées gauche et supérieure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




