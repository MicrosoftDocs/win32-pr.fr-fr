---
description: La méthode GetWindowPosition récupère les coordonnées actuelles de la fenêtre.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Méthode CBaseControlWindow. GetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d576f065e807c2af47621d43940d7e48c54f36f0617d20590953a5e83ab2fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966729"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a>Méthode CBaseControlWindow. GetWindowPosition

La `GetWindowPosition` méthode récupère les coordonnées actuelles de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetWindowPosition(
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

Pointeur vers la coordonnée gauche, en coordonnées d’écran.

</dd> <dt>

*pTop* 
</dt> <dd>

Pointeur vers la coordonnée supérieure, en coordonnées d’écran.

</dd> <dt>

*pWidth* 
</dt> <dd>

Pointeur vers la largeur de la fenêtre, en coordonnées d’écran.

</dd> <dt>

*pHeight* 
</dt> <dd>

Pointeur vers la hauteur de la fenêtre, en coordonnées d’écran.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




