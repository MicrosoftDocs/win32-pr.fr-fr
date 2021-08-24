---
description: La \_ méthode put Top définit la coordonnée supérieure de la fenêtre.
ms.assetid: cd39807f-363d-4b5b-8279-9dfb992dca10
title: Méthode CBaseControlWindow.put_Top (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Top
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3332bcf90ac5e2ee776fe7110c958e50b838bcbdbc6bb4abb23850ced12cc28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635829"
---
# <a name="cbasecontrolwindowput_top-method"></a>CBaseControlWindow. put \_ Top, méthode

La `put_Top` méthode définit la coordonnée supérieure de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Top(
   long Top
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Top* 
</dt> <dd>

Nouvelle coordonnée supérieure, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

La fenêtre a une position sur le bureau. Ce pourcentage est exprimé en pixels par quatre coordonnées (gauche, haut, droit et bas). Les interfaces automatisées par OLE expriment généralement cette position à gauche, en haut, à largeur et en hauteur ; Il s’agit de la Convention utilisée dans DirectShow. Toutes les coordonnées sont exprimées en pixels, et la modification de toute coordonnée met immédiatement à jour la fenêtre.

La définition des coordonnées gauche ou supérieure déplace la fenêtre vers la gauche ou vers le haut, respectivement ; ces coordonnées n’ont aucun effet sur la largeur et la hauteur de la fenêtre. De même, la définition de la largeur et de la hauteur n’affecte pas les coordonnées gauche et supérieure.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




