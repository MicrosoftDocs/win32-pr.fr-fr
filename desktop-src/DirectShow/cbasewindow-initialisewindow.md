---
description: La méthode InitialiseWindow initialise la fenêtre.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Iniméthode tialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545472"
---
# <a name="cbasewindowinitialisewindow-method"></a>CBaseWindow.Iniméthode tialiseWindow

La `InitialiseWindow` méthode initialise la fenêtre.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK.

## <a name="remarks"></a>Notes

Par défaut, cette méthode récupère un handle vers le contexte de périphérique (DC) de la fenêtre et crée un DC de mémoire compatible. Toutefois, si la valeur de l’indicateur [**CBaseWindow :: m \_ BDoGetDC**](cbasewindow-m-bdogetdc.md) est **false**, cette méthode ne récupère pas les contextes de périphérique. Le DC de mémoire est utile pour sélectionner des bitmaps avant de les blitting dans la fenêtre.

La méthode [**CBaseWindow ::D ocreatewindow**](cbasewindow-docreatewindow.md) appelle cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




