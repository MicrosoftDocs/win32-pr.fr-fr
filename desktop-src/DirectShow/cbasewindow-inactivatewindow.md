---
description: La méthode InactivateWindow désactive la fenêtre. Dans la classe de base, cette méthode masque la fenêtre.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Méthode CBaseWindow. InactivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1c5e925a3d9b510918636a221d5ad6e1b7da736
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542574"
---
# <a name="cbasewindowinactivatewindow-method"></a>Méthode CBaseWindow. InactivateWindow

La `InactivateWindow` méthode désactive la fenêtre. Dans la classe de base, cette méthode masque la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.



| Code de retour                                                                             | Description                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Opération réussie.<br/>                    |
| <dl> <dt>**S \_ false**</dt> </dl> | La fenêtre est déjà inactive.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




