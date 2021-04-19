---
description: La méthode PaintWindow provoque la redessin de la fenêtre.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Méthode CBaseWindow. PaintWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539250"
---
# <a name="cbasewindowpaintwindow-method"></a>Méthode CBaseWindow. PaintWindow

La `PaintWindow` méthode permet de redessiner la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bErase* 
</dt> <dd>

Valeur booléenne qui spécifie si l’arrière-plan est effacé. Si la valeur est **true**, l’arrière-plan est effacé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode génère un \_ message WM Paint en invalidant la zone cliente entière de la fenêtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




