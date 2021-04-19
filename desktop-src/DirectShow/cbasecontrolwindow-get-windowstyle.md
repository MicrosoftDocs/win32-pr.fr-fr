---
description: La \_ méthode obtenir WindowStyle récupère les styles de fenêtre standard.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: Méthode CBaseControlWindow.get_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91e04efac3a67c262b4eeb85948f846dbb06086a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542739"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a>CBaseControlWindow. obten, \_ méthode WindowStyle

La `get_WindowStyle` méthode récupère les styles de fenêtre standard.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pWindowStyle* 
</dt> <dd>

Pointeur vers les styles de fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre retourne les styles de fenêtre standard, tels que WS \_ Child et WS \_ visible. Elle appelle la fonction membre [**CBaseControlWindow ::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




