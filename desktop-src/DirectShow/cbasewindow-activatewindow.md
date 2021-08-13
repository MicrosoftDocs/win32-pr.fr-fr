---
description: La méthode ActivateWindow dimensionne la fenêtre en fonction des exigences de la classe dérivée.
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: Méthode CBaseWindow. ActivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e00c3ccc43e2583ce8664e62967a22f753148cfa271dd1995e2374c2bfa53c71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658243"
---
# <a name="cbasewindowactivatewindow-method"></a>Méthode CBaseWindow. ActivateWindow

La `ActivateWindow` méthode dimensionne la fenêtre en fonction des spécifications de la classe dérivée.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | La fenêtre a déjà été activée.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                      |



 

## <a name="remarks"></a>Remarques

Cette méthode appelle la méthode [**CBaseWindow :: GetDefaultRect**](cbasewindow-getdefaultrect.md) pour déterminer la taille de la fenêtre. La classe dérivée doit substituer **GetDefaultRect** pour retourner la taille des images qui seront affichées.

Si la fenêtre est déjà active, l’appel `ActivateWindow` de déplace la fenêtre vers le haut de l’ordre de plan, mais ne redimensionne pas la fenêtre. Il en va de même si la fenêtre a un parent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




