---
description: La méthode UninitialiseWindow libère les ressources de la fenêtre.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Méthode CBaseWindow. UninitialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545679"
---
# <a name="cbasewindowuninitialisewindow-method"></a>Méthode CBaseWindow. UninitialiseWindow

La `UninitialiseWindow` méthode libère les ressources de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode libère les ressources acquises par la méthode [**CBaseWindow :: InitialiseWindow**](cbasewindow-initialisewindow.md) . La méthode [**CBaseWindow ::D onewithwindow**](cbasewindow-donewithwindow.md) appelle cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




