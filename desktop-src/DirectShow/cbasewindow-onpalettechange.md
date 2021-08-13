---
description: La méthode OnPaletteChange gère les messages de modification de palette.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Méthode CBaseWindow. OnPaletteChange (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c881c519706ca0288847a7dc603cf513a99cdd76e4c83f0e53bec16df840e509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657952"
---
# <a name="cbasewindowonpalettechange-method"></a>Méthode CBaseWindow. OnPaletteChange

La `OnPaletteChange` méthode gère les messages de modification de palette.

## <a name="syntax"></a>Syntaxe


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle vers la fenêtre.

</dd> <dt>

*Message* 
</dt> <dd>

Identificateur du message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 si le message a été traité, ou 1 si le message n’a pas été traité.

## <a name="remarks"></a>Remarques

Cette méthode gère \_ les messages WM PALETTECHANGED et WM \_ QUERYNEWPALETTE. Elle appelle la méthode [**CBaseWindow ::D orealisepalette**](cbasewindow-dorealisepalette.md) pour réaliser la nouvelle palette.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Winutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseWindow, classe**](cbasewindow.md)
</dt> </dl>

 

 




