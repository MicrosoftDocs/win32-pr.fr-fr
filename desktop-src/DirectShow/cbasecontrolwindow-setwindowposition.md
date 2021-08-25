---
description: La méthode SetWindowPosition définit la position de la fenêtre sur le bureau.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Méthode CBaseControlWindow. SetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2734c93d1a3d3d3ea29e037d1bf85baacd5358a69f08d1517012c3eb250ab8ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635458"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a>Méthode CBaseControlWindow. SetWindowPosition

La `SetWindowPosition` méthode définit la position de la fenêtre sur le bureau.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Left* 
</dt> <dd>

Nouvelle coordonnée gauche.

</dd> <dt>

*Top* 
</dt> <dd>

Nouvelle coordonnée supérieure.

</dd> <dt>

*Width* 
</dt> <dd>

Largeur de la fenêtre.

</dd> <dt>

*Height* 
</dt> <dd>

Hauteur de la fenêtre.

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

 

 




