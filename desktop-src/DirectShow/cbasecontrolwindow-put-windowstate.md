---
description: La \_ méthode put WindowState définit l’état de la fenêtre.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: Méthode CBaseControlWindow.put_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521763"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a>Méthode CBaseControlWindow. put \_ WindowState

La `put_WindowState` méthode définit l’état de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*WindowState* 
</dt> <dd>

Nouvel état de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre accepte les mêmes paramètres que la fonction Microsoft Win32 **ShowWindow** (par exemple, WS \_ SHOWNORMAL, WS \_ SHOWMINNOACTIVATE et WS \_ SHOWMAXIMIZED).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




