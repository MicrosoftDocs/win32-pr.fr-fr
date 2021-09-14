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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123806"
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

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction membre accepte les mêmes paramètres que la fonction Microsoft Win32 **ShowWindow** (par exemple, WS \_ SHOWNORMAL, WS \_ SHOWMINNOACTIVATE et WS \_ SHOWMAXIMIZED).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




