---
description: La \_ méthode put Left définit la coordonnée gauche de la fenêtre.
ms.assetid: 4ba6b243-e7a7-4c41-a2c5-248b05b42f4f
title: Méthode CBaseControlWindow.put_Left (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Left
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1dcd56bc10e60d263ce385246a6ea01aee721bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123809"
---
# <a name="cbasecontrolwindowput_left-method"></a>CBaseControlWindow. put \_ Left, méthode

La `put_Left` méthode définit la coordonnée gauche de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Left(
   long Left
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Left* 
</dt> <dd>

Nouvelle coordonnée gauche, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

La fenêtre a une position sur le bureau. Ce pourcentage est exprimé en pixels par quatre coordonnées (gauche, haut, droit et bas). Les interfaces automatisées par OLE expriment généralement cette position à gauche, en haut, à largeur et en hauteur ; Il s’agit de la Convention utilisée dans DirectShow. Toutes les coordonnées sont exprimées en pixels, et la modification de toute coordonnée met immédiatement à jour la fenêtre.

La définition des coordonnées gauche ou supérieure déplace la fenêtre vers la gauche ou vers le haut, respectivement ; ces coordonnées n’ont aucun effet sur la largeur et la hauteur de la fenêtre. De même, la définition de la largeur et de la hauteur n’affecte pas les coordonnées gauche et supérieure.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




