---
description: La méthode PerformanceAlignWindow aligne la position de la fenêtre sur les limites DWORD, pour des performances maximales.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Méthode CBaseWindow. PerformanceAlignWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542750"
---
# <a name="cbasewindowperformancealignwindow-method"></a>Méthode CBaseWindow. PerformanceAlignWindow

La `PerformanceAlignWindow` méthode aligne la position de la fenêtre sur les limites **DWORD** , pour des performances maximales.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Cette méthode aligne les bords gauche et supérieur de la fenêtre sur les limites DWORD, ce qui peut améliorer les performances. Si la fenêtre a un parent, la méthode retourne S \_ OK, mais effectue l’alignement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




