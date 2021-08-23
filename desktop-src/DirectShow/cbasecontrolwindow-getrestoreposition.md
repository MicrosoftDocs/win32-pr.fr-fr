---
description: La méthode GetRestorePosition récupère la position vers laquelle la fenêtre sera restaurée lorsqu’elle n’est pas agrandie ou réduite.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Méthode CBaseControlWindow. GetRestorePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 215b71d731227641df02716dd2b760f7e023bbec0c50bc66ac6d390ed87d002e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757609"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a>Méthode CBaseControlWindow. GetRestorePosition

La `GetRestorePosition` méthode récupère la position vers laquelle la fenêtre sera restaurée lorsqu’elle n’est pas agrandie ou réduite.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pLeft* 
</dt> <dd>

Pointeur vers la valeur de la coordonnée la plus à gauche.

</dd> <dt>

*pTop* 
</dt> <dd>

Pointeur vers la valeur pour le haut de la fenêtre.

</dd> <dt>

*pWidth* 
</dt> <dd>

Pointeur vers la valeur pour la largeur de la fenêtre.

</dd> <dt>

*pHeight* 
</dt> <dd>

Pointeur vers la valeur de la hauteur de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Remarques

Il s’agit des mêmes valeurs que celles retournées par la fonction [**CBaseControlWindow :: GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) lorsque la fenêtre n’est ni agrandie, ni réduite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




