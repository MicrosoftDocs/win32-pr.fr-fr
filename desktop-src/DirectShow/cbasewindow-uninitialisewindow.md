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
ms.openlocfilehash: c275e4d683bcc698c8f04c5a85017b081b6aad17f93c91d66e0a75f2da88692e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657491"
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

## <a name="remarks"></a>Remarques

Cette méthode libère les ressources acquises par la méthode [**CBaseWindow :: InitialiseWindow**](cbasewindow-initialisewindow.md) . La méthode [**CBaseWindow ::D onewithwindow**](cbasewindow-donewithwindow.md) appelle cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




