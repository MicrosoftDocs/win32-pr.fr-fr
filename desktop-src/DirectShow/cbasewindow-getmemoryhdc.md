---
description: La méthode GetMemoryHDC récupère un handle vers le contexte de périphérique (DC) de mémoire.
ms.assetid: 2c22015f-5948-4e1a-92c7-36f232816175
title: Méthode CBaseWindow. GetMemoryHDC (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetMemoryHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c255ac8734f364597c09fc15b4aa543b1ec0a0da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542575"
---
# <a name="cbasewindowgetmemoryhdc-method"></a>Méthode CBaseWindow. GetMemoryHDC

La `GetMemoryHDC` méthode récupère un handle vers le contexte de périphérique (DC) de mémoire.

## <a name="syntax"></a>Syntaxe


```C++
virtual HDC GetMemoryHDC();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne un handle vers le DC de mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




