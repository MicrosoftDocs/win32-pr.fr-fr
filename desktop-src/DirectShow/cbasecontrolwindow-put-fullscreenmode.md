---
description: La \_ méthode put FullScreenMode définit le mode plein écran du convertisseur.
ms.assetid: 25e2a12e-a327-4aab-b4ab-54db0dfc950a
title: Méthode CBaseControlWindow.put_FullScreenMode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_FullScreenMode
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d1af1a6a4e4b77521d3f27ff5c94651048d6d75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094838"
---
# <a name="cbasecontrolwindowput_fullscreenmode-method"></a>CBaseControlWindow. put \_ FullScreenMode, méthode

La `put_FullScreenMode` méthode définit le mode plein écran du convertisseur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_FullScreenMode(
   long FullScreenMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FullScreenMode* 
</dt> <dd>

Mode plein écran à appliquer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . L’implémentation actuelle retourne E \_ NOTIMPL.

## <a name="remarks"></a>Notes

Un convertisseur vidéo qui implémente un mode plein écran doit substituer cette fonction membre et implémenter les modes pris en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




