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
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521640"
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
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                      |



 

## <a name="remarks"></a>Notes

Cette méthode appelle la méthode [**CBaseWindow :: GetDefaultRect**](cbasewindow-getdefaultrect.md) pour déterminer la taille de la fenêtre. La classe dérivée doit substituer **GetDefaultRect** pour retourner la taille des images qui seront affichées.

Si la fenêtre est déjà active, l’appel `ActivateWindow` de déplace la fenêtre vers le haut de l’ordre de plan, mais ne redimensionne pas la fenêtre. Il en va de même si la fenêtre a un parent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




