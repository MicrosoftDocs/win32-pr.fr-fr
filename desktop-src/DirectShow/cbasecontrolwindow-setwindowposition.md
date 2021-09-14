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
ms.openlocfilehash: d5e92581db4d04d622f5dba5fbfe1c2c4a53b4ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296826"
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

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




