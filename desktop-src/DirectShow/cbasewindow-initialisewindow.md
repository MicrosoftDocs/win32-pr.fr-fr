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
ms.openlocfilehash: f260f60111f715bfce357e264b65bb4b821c5ca890d39d4d54e7269a191df303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954658"
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

Handle vers la fenêtre.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne S \_ OK.

## <a name="remarks"></a>Remarques

Par défaut, cette méthode récupère un handle vers le contexte de périphérique (DC) de la fenêtre et crée un DC de mémoire compatible. Toutefois, si la valeur de l’indicateur [**CBaseWindow :: m \_ BDoGetDC**](cbasewindow-m-bdogetdc.md) est **false**, cette méthode ne récupère pas les contextes de périphérique. Le DC de mémoire est utile pour sélectionner des bitmaps avant de les blitting dans la fenêtre.

La méthode [**CBaseWindow ::D ocreatewindow**](cbasewindow-docreatewindow.md) appelle cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




