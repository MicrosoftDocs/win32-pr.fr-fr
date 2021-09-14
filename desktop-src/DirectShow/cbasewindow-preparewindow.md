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
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923703"
---
# <a name="cbasewindowpreparewindow-method"></a>Méthode CBaseWindow. PrepareWindow

La `PrepareWindow` méthode crée la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                            | Description         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl> | Échec.<br/> |



 

## <a name="remarks"></a>Notes

Appelez cette méthode après avoir créé l’objet. Cette méthode effectue une comptabilité initiale, puis appelle la méthode [**CBaseWindow ::D ocreatewindow**](cbasewindow-docreatewindow.md) pour créer la fenêtre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




