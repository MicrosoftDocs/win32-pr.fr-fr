---
description: La méthode PrepareWindow crée la fenêtre.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Méthode CBaseWindow. PrepareWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b2811e307b370323c331d3f894116ad0ff01af25ad76e1ea775dae5489dfb15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074563"
---
# <a name="cbasewindowpreparewindow-method"></a>Méthode CBaseWindow. PrepareWindow

La `PrepareWindow` méthode crée la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                            | Description         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl> | Échec.<br/> |



 

## <a name="remarks"></a>Remarques

Appelez cette méthode après avoir créé l’objet. Cette méthode effectue une comptabilité initiale, puis appelle la méthode [**CBaseWindow ::D ocreatewindow**](cbasewindow-docreatewindow.md) pour créer la fenêtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




