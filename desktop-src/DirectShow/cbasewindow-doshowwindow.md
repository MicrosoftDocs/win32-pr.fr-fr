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
ms.openlocfilehash: 7fef63e04d0e04f2fe0daa78cd6b33a22fa7c8fa14c57b1e022703dea0914dab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074626"
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
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

