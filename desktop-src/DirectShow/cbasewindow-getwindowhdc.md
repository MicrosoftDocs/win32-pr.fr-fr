---
description: La méthode GetWindowHDC récupère un handle vers le contexte de périphérique (DC) de la fenêtre.
ms.assetid: 35ee2a66-ee56-44dc-ad59-fd467bb4aa63
title: Méthode CBaseWindow. GetWindowHDC (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetWindowHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff0129e63e9a0c9808e36d73e37ff0e76d712b64c18e1e37ef88105797e2b495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074603"
---
# <a name="cbasewindowgetwindowhdc-method"></a>Méthode CBaseWindow. GetWindowHDC

La `GetWindowHDC` méthode récupère un handle vers le contexte de périphérique (DC) de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HDC GetWindowHDC();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un handle vers le DC.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




