---
description: La méthode OnSize gère les \_ messages de taille WM.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Méthode CBaseWindow. OnSize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf6c7793af3cb7866ddaaaae8823acd91ed10ac71d939af8bc9e71eff768d75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657654"
---
# <a name="cbasewindowonsize-method"></a>Méthode CBaseWindow. OnSize

La `OnSize` méthode gère les \_ messages de taille WM.

## <a name="syntax"></a>Syntaxe


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Width* 
</dt> <dd>

Largeur de la zone cliente, en pixels.

</dd> <dt>

*Height* 
</dt> <dd>

Hauteur de la zone cliente, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true**.

## <a name="remarks"></a>Remarques

Cette méthode stocke les nouvelles largeur et hauteur. Pour récupérer ces valeurs, appelez les méthodes [**CBaseWindow :: GetWindowHeight**](cbasewindow-getwindowheight.md) et [**CBaseWindow :: GetWindowWidth**](cbasewindow-getwindowwidth.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




