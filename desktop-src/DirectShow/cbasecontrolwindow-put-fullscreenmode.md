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
ms.openlocfilehash: 2e7aa121ce78198fe6b2ca0b88109183665f0cd93dd95294a848a2b2d0c03548
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983679"
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

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . L’implémentation actuelle retourne E \_ NOTIMPL.

## <a name="remarks"></a>Remarques

Un convertisseur vidéo qui implémente un mode plein écran doit substituer cette fonction membre et implémenter les modes pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




