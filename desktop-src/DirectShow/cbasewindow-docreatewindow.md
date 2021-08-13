---
description: La méthode DoCreateWindow crée la fenêtre.
ms.assetid: bbe38a71-bbf7-4380-96a3-074b992a1d1e
title: CBaseWindow.DoCméthode reateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoCreateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2502d1c07efbb5fa15c8113d11504b9a61a64321686e2b0e7e4939fabad7395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658223"
---
# <a name="cbasewindowdocreatewindow-method"></a>CBaseWindow.DoCméthode reateWindow

La `DoCreateWindow` méthode crée la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DoCreateWindow();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite, ou une valeur **HRESULT** indiquant la cause de l’échec.

## <a name="remarks"></a>Remarques

La méthode [**CBaseWindow ::P reparewindow**](cbasewindow-preparewindow.md) appelle cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




