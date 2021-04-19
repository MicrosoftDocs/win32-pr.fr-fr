---
description: La méthode DoShowWindow définit l’état d’affichage de la fenêtre.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Méthode CBaseWindow. DoShowWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2a1f7d4cd9bc4600733d5d33f9df6d3b6998f57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544090"
---
# <a name="cbasewindowdoshowwindow-method"></a>Méthode CBaseWindow. DoShowWindow

La méthode **DoShowWindow** définit l’état d’affichage de la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ShowCmd* 
</dt> <dd>

Indicateur qui spécifie la façon dont la fenêtre doit être affichée. La valeur peut être toute constante définie pour le paramètre *nCmdShow* de la fonction [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

