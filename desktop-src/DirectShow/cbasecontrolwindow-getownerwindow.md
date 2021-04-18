---
description: La méthode GetOwnerWindow récupère le handle de fenêtre propriétaire, m \_ hwndOwner.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Méthode CBaseControlWindow. GetOwnerWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533069"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a>Méthode CBaseControlWindow. GetOwnerWindow

La `GetOwnerWindow` méthode récupère le handle de fenêtre propriétaire, **m \_ hwndOwner**.

## <a name="syntax"></a>Syntaxe


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne la fenêtre propriétaire.

## <a name="remarks"></a>Notes

Récupère la fenêtre propriétaire sans appeler la méthode d’interface. Utilisez cette fonction membre à la place de [**CBaseControlWindow :: obten \_ owner**](cbasecontrolwindow-get-owner.md), sauf si vous appelez cette méthode en externe par le biais de la méthode [**IVideoWindow :: d’extraction de \_ propriétaire**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




