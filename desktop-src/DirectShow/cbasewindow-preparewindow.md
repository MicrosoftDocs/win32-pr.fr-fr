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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540664"
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
| <dl> <dt>**\_OK**</dt> </dl>   | Opération réussie.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl> | Échec.<br/> |



 

## <a name="remarks"></a>Notes

Appelez cette méthode après avoir créé l’objet. Cette méthode effectue une comptabilité initiale, puis appelle la méthode [**CBaseWindow ::D ocreatewindow**](cbasewindow-docreatewindow.md) pour créer la fenêtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




